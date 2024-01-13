---
title: Version 1906 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 1906. 
ms.date: 07/19/2019
ms.topic: conceptual
ms.author: banreetkaur
author: Banreet
manager: apoorvseth
ROBOTS: NOINDEX
---

# Configuration Manager Cmdlet Library changes for version 1906

*Applies to: Configuration Manager (Current Branch)*

> [!NOTE]  
> Configuration Manager current branch version 1902 is the baseline for these changes. For more information, see [Configuration Manager Cmdlet Library changes for version 1902](1902-release-notes.md).


## Important changes

### New cmdlets

#### Get-CMTSStepRunTaskSequence

Use this cmdlet to get the **Run Task Sequence** step from a specific task sequence.

```PowerShell
$myStep = $ReferenceTaskSequence | Get-CMTSStepRunTaskSequence -StepName $name1
```

#### New-CMSoftwareCenterTabItem

Use this cmdlet to create a custom Software Center tab.

```PowerShell
$itemA = New-CMSoftwareCenterTabItem -Name "1abc" -Url http://www.a
```

#### New-CMTSStepRunTaskSequence

Use this cmdlet to create the task sequence step **Run Task Sequence**.

```PowerShell
$myStep = New-CMTSStepRunTaskSequence - Name $name1 -RunTaskSequence $refSubTaskSequence
```

#### Remove-CMTSStepRunTaskSequence

Use cmdlet to remove the task sequence step **Run Task Sequence** from a specific task sequence.

```PowerShell
$ReferenceTaskSequence | Remove-CMTSStepRunTaskSequence -StepName $myStep.Name -Force
```

#### Set-CMScript

Use this cmdlet to edit a script.

```PowerShell
Get-CMScript -ScriptName $name | Set-CMScript -ScriptFile $file
```

#### Set-CMTSStepRunTaskSequence

Use this cmdlet to edit the task sequence **step Run Task Sequence**.

```PowerShell
$ReferenceTaskSequence | Set-CMTSStepRunTaskSequence -RunTaskSequence $refSubTaskSequence
```

### Removed cmdlets

None

### Deprecated cmdlets

- Get-CMAadConditionalAccessPolicy
- Set-CMAadConditionalAccessPolicy


## Known issues

The following items are known issues with the Cmdlet Library that aren't resolved in this version.

### Import-CMSecurityRole

Cmdlet may fail with a DirectoryNotFoundException error locating the file `SecuredRoles.xsd`.

#### Workaround

- Call `Import-Module` against the `ConfigurationManager.psd1` file, and not the logical path or module name.

### Set-CMSoftwareUpdatePoint

Changes to **Schedule** may not be shown in the Configuration Manager console even though the underlying SMS Provider object has been changed.

#### Workaround

- Quit and relaunch the Configuration Manager console.

### Resource tracking and recovery (beta)

This version adds new cmdlets to support tracking SMS Provider objects used by the PowerShell runtime, and to clean up these resources when they're no longer needed.

- Disconnect-CMTrackedObject
- Start-CMObjectTracking
- Stop-CMObjectTracking

When you run `Start-CMObjectTracking`, the PowerShell runtime tracks `IResultObject` objects created by Cmdlet Library cmdlets. For cmdlets that aren't manually cleaned up with `.Dispose()`, reclaim them by using `Disconnect-CMTrackedObject` against an individual object.

#### Example

```powershell
# Reclaim a single tracked object
$o | Disconnect-CMTrackedObject

# Reclaim all tracked objects
Disconnect-CMTrackedObject -All
```

Once an object is reclaimed, it can no longer be reused or passed to another cmdlet through the object pipeline.

`Stop-CMObjectTracking` can be used to turn off object tracking. Previously allocated objects remain active.

Unclaimed resources can cause the SMS Provider to raise quota violation errors. These quota issues typically manifest from working with large sets of SMS Provider objects or in long-running environments.

> [!NOTE]  
> This feature is experimental and may be subject to change or removal in a future release. It's opt-in and isn't enabled by default.  


## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

### Add-CMComplianceSettingScript

#### Bugs that were fixed

- Missing options to support remediate.

#### Non-breaking changes

- Added parameter to support remediate: `-Remediate`

##### Example

```Powershell
Add-CMComplianceSettingScript -InputObject $ci -DiscoveryScriptLanguage PowerShell -DataType String -Name "test1" -DiscoveryScriptText "test" -RemediationScriptLanguage PowerShell -RemediationScriptText "test"  -RuleName rule1 -ExpressionOperator IsEquals -ValueRule -ExpectedValue 1.0 -Remediate
```

### Add-CMDeviceCollectionDirectMembershipRule

#### Bugs that were fixed

- Cmdlet failed when you tried to apply hundreds of direct rules.

#### Non-breaking changes

- Separated the queries from different classes to improve the performance.

### Add-CMMsiDeploymentType

#### Bugs that were fixed

- The behavior wasn't consistent with the console when the cmdlet changes the logon requirement settings.
- Missing application properties.
- You may specify wrong value for `-LogonRequirementType` and `-RequireUserInteraction` when they specify `-InstallationBehaviorType InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser`

#### Non-breaking changes

- Modified the validation logic for the "User Experience" settings: the "User Interaction" would be blocked only when you specified "no user logon" as the logon requirement.
- Added application properties: `CategoryInstance_UniqueIDs` and `Featured`
- Added combination logic to address issues in `-LogonRequirementType`, `-RequireUserInteraction`, and `-InstallationBehaviorType`

### Add-CMScriptDeploymentType

#### Bugs that were fixed

- Failed when specify null value to `-AddRequirement`.
- Missing application properties.

#### Non-breaking changes

- Added parameter validation for null value.
- Added application properties: `CategoryInstance_UniqueIDs` and `Featured`

### Add-CMUserCollectionDirectMembershipRule

#### Bugs that were fixed

- Cmdlet failed when you tried to apply hundreds of direct rules.

#### Non-breaking changes

- Separated the queries from different classes to improve the performance.

### Import-CMDriver

#### Bugs that were fixed

- Cmdlet doesn't work correctly.

#### Non-breaking changes

- Fixed unhandled exception issue.
- Fixed source path issue to align with console.

### Import-CMDriverPackage

#### Bugs that were fixed

- The `-ImportActionType` parameter would set same import action for all objects.

#### Non-breaking changes

- Cmdlet would import object by using default action if you didn't specify one.
- Added new parameter to support specifying import action type for different classes of object: `-ImportActionTypeSpec`

##### Example

```PowerShell
# Specify import action type for different classes of object:
$classVsAction = @{"SMS_Driver" = [Microsoft.ConfigurationManagement.AdminConsole.MigrationAssistant.ImportActionType]::AppendDriverCategories}
Import-CMDriverPackage -ImportFilePath $filePath -ImportActionTypeSpec $classVsAction
```

### Import-CMTaskSequence

#### Bugs that were fixed

- The `-ImportActionType` parameter would set same import action for all objects.

#### Non-breaking changes

- Cmdlet would import object by using default action if didn't specify one.
- Added new parameter to support specifying import action type for different classes of object: `-ImportActionTypeSpec`

### Invoke-CMClientAction

#### Bugs that were fixed

- Cmdlet with parameter `-DeviceName`, `-DeviceId`, or `-Device` would fail if you don't have permission to "All Systems" collection.
- Missing options to wake up machine.

#### Non-breaking changes

- Removed the collection permission limitation to align with console.
- Added new parameters to support waking up machine:
    - `-ParentCollectionId`
    - `-ParentCollectionName`
    - `-ParentCollection`

##### Example

```PowerShell
# Wake up machine:
Invoke-CMClientAction -DeviceName "SleepDevice01" -ActionType ClientNotificationWakeUpClientNow -ParentCollectionId $col.CollectionID
```

### Invoke-CMEndpointProtectionScan

#### Bugs that were fixed

- Cmdlet with parameter `-DeviceName`, `-DeviceId`, or `-Device` would fail if you don't have permission to "All Systems" collection.

#### Non-breaking changes

- Removed the collection permission limitation to align with console.

### Invoke-CMQuery

#### Bugs that were fixed

- Invoke-CMQuery command didn't respect the `-LimitToCollectionID` parameter.

#### Non-breaking changes

- Supported empty value for parameter `-LimitToCollectionID` in CMquery object.

### Get-CMApplicationDeployment

#### Bugs that were fixed

- Cmdlet would unexpectedly destroy object with `-InputObect`.

#### Non-breaking changes

- Fixed the object dispose issue.

### New-CMApplication

#### Bugs that were fixed

- Failed to set icon that size is greater than 250x250.

#### Non-breaking changes

- Extended the icon size to 512x512 to align with console.

### New-CMApplicationDeployment

#### Bugs that were fixed

- Cmdlet would unexpectedly destroy object with `-InputObect`.

#### Non-breaking changes

- Fixed the object dispose issue.

### New-CMApplicationDisplayInfo

#### Bugs that were fixed

- Failed to set icon that size is greater than 250x250.

#### Non-breaking changes

- Extended the icon size to 512x512 to align with console.

### New-CMAutoDeploymentRuleDeployment

#### Bugs that were fixed

- Missing parameters for "Allow WUMU" and "Allow Use Metered Network" options.
- Missing parameters for "DelayGracePeriod" and "SoftwareUpdatesBehaviorOfRestart"
- Missing validation for date time units input.

#### Non-breaking changes

- Added new parameters to support set "Allow WUMU" and "Allow Use Metered Network" options:
    - `-AllowDownloadFromMicrosoftUpdate`
    - `-AllowUseMeteredNetwork`
- Added new parameters to support set "DelayGracePeriod" and "SoftwareUpdatesBehaviorOfRestart" options:
    - `-SoftDeadlineEnabled`
    - `-RequirePostRebootFullScan`
- Added validation for available and deadline with specific unit.

### New-CMBaseline

#### Bugs that were fixed

- Need option to support "Apply on co-management client".

#### Non-breaking changes

- Added new parameter to support the option "Apply on co-management client":
    - `-AllowComanagedClients`

### New-CMBootableMedia

#### Bugs that were fixed

- Need option to support "Ability to not include Autorun.inf".

#### Non-breaking changes

- Added new parameter to support the option "Ability to not include Autorun.inf":
    - `-NoAutoRun`

### New-CMCaptureMedia

#### Bugs that were fixed

- Need option to support "Ability to not include Autorun.inf".

#### Non-breaking changes

- Added new parameter to support the option "Ability to not include Autorun.inf":
    - `-NoAutoRun`

### New-CMPackage

#### Bugs that were fixed

- Cmdlet may set oversize text in package info.

#### Non-breaking changes

- Added length validation for string values to align with console.

### New-CMPackageDeployment

#### Bugs that were fixed

- Cmdlet failed because of wrong property name.

#### Non-breaking changes

- Fixed property name issue.

### New-CMPrestageMedia

#### Bugs that were fixed

- Need option to support "Ability to not include Autorun.inf".

#### Non-breaking changes

- Added new parameter to support the option "Ability to not include Autorun.inf":
    - `-NoAutoRun`

### New-CMRequirementRuleCommonValue

#### Bugs that were fixed

- Evaluation failed on the deployment type when you specify requirement rule with common value.

#### Non-breaking changes

- Fixed the string value issue to prevent '/r/n' in single string.

### New-CMSchedule

#### Bugs that were fixed

- Missing offset day option.

#### Non-breaking changes

- Added parameter OffsetDay for supporting the offset in monthlybyweekday.

##### Example

```PowerShell
New-CMSchedule -Start (Get-Date) -DayOfWeek Monday -WeekOrder Second -RecurCount 1 -OffsetDay 0
```

### New-CMSoftwareUpdateAutoDeploymentRule

#### Bugs that were fixed

- You couldn't add third-party catalogs to auto deployment rule with this cmdlet.
- Missing Office 365 language selection.
- Missing filter options: "Architecture" and "Content Size".
- Missing validation for available and deadline time with units.
- Failed to set $false to `-EnableAfterCreate`.
- Default values for language selection didn't align with console.

#### Non-breaking changes

- Added vendor support for third-party updates.
- Added new parameter for Office 365 language selection to align with console:
    - `-O365LanguageSelection`
- Added new parameter for filter options "Architecture" and "Content Size":
    - `-Architecture`
    - `-ContentSize`
- Added validation for available and deadline time with units.
- Fixed the logic to set `-EnableAfterCreate`.
- Changed the default values for language selection to align with console.

##### Example

```PowerShell
# Set filter "Architecture":
$newADR = New-CMSoftwareUpdateAutoDeploymentRule -Collection $collection -DeploymentPackageName $PackageName -Name $name -Architecture X86, Itanium, X64

# Set filter "Content Size":
$newADR = New-CMSoftwareUpdateAutoDeploymentRule -Collection $collection -DeploymentPackageName $PackageName -Name $name -ContentSize $size
```

### New-CMSoftwareUpdateDeployment

#### Bugs that were fixed

- Missing option for "DelayGracePeriod".

#### Non-breaking changes

- Added new parameter for option "DelayGracePeriod":
    - `-SoftDeadlineEnabled`

### New-CMStandaloneMedia

#### Bugs that were fixed

- Need option to support "Ability to not include Autorun.inf".

#### Non-breaking changes

- Added new parameter to support the option "Ability to not include Autorun.inf":
    - `-NoAutoRun`

### New-CMStatusFilterRule

#### Bugs that were fixed

- `-PropertyId` failed "Exception not caught: System.ArgumentOutOfRangeException".

#### Non-breaking changes

- Added validation for Source/PropertyID/PropertyValue to avoid invalid input.

### New-CMTSStepApplyNetworkSetting

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### New-CMTSStepApplyWindowsSettings

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### New-CMTSStepCaptureSystemImage

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### New-CMTSStepConnectNetworkFolder

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### New-CMTSStepDisableBitLocker

#### Bugs that were fixed

- Need option to set "Reboot Count"

#### Non-breaking changes

- Added new parameter for "Reboot Count" option:
    - `-RebootCount`

### New-CMTSStepEnableBitLocker

#### Bugs that were fixed

- Task sequence step with user PIN failed when task sequence running.
- Missing parameter for "Use full disk encryption" option.

#### Non-breaking changes

- Fixed security object issue.
- Added new parameter for "Use full disk encryption" option:
    - `-EncryptFullDisk`

### New-CMTSStepInstallApplication

#### Bugs that were fixed

- Need option to install application step to clear its content from cache after installing the application.

#### Non-breaking changes

- Added new parameter to clear its content from cache after installing the application:
    - `-ClearCache`

### New-CMTSStepJoinDomainWorkgroup

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### New-CMTSStepRestoreUserState

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### New-CMTSStepRunCommandLine

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### New-CMTSStepRunPowerShellScript

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### New-CMWindowsFirewallPolicy

#### Bugs that were fixed

- Options shouldn't be configured when related firewall settings weren't set.

#### Non-breaking changes

- Added code to check firewall setting for dependent parameters.

### Remove-CMSoftwareUpdatePoint

#### Bugs that were fixed

- WCM wasn't reset after you ran the cmdlet to delete a software update point.

#### Non-breaking changes

- Added logic to reset the WCM when you delete a software update point.

### Set-CMApplication

#### Bugs that were fixed

- Failed to set icon that size is greater than 250x250.

#### Non-breaking changes

- Extended the icon size to 512x512 to align with console.

### Set-CMAutoDeploymentRuleDeployment

#### Bugs that were fixed

- Missing parameters for "Allow WUMU" and "Allow Use Metered Network" options.
- Missing parameters for "DelayGracePeriod" and "SoftwareUpdatesBehaviorOfRestart"
- Missing validation for date time units input.

#### Non-breaking changes

- Added new parameters to support set "Allow WUMU" and "Allow Use Metered Network" options:
    - `-AllowDownloadFromMicrosoftUpdate`
    - `-AllowUseMeteredNetwork`
- Added new parameters to support set "DelayGracePeriod" and "SoftwareUpdatesBehaviorOfRestart" options:
    - `-SoftDeadlineEnabled`
    - `-RequirePostRebootFullScan`
- Added validation for available and deadline with specific unit.

### Set-CMBaseline

#### Bugs that were fixed

- Need option to support "Apply on co-management client".

#### Non-breaking changes

- Added new parameter to support the option "Apply on co-management client":
    - `-AllowComanagedClients`

### Set-CMClientSettingPowerManagement

#### Bugs that were fixed

- Missing parameter for "Allow network wake-up" option.

#### Non-breaking changes

- Added new parameter to support network wakeup:
    - `-NetworkWakeupOption`

##### Example

```PowerShell
Set-CMClientSettingPowerManagement -Name "test settings" -AllowUserToOptOutFromPowerPlan $true -EnableWakeupProxy $true -NetworkWakeupOption Enabled -WakeupProxyPort 25511 -WakeOnLanPort 10 -FirewallExceptionForWakeupProxy None
```

### Set-CMClientSettingSoftwareCenter

#### Bugs that were fixed

- Support custom tab feature.

#### Non-breaking changes

- Added new parameters to support custom tab operation:
    - `-ClearCustomTab`
    - `-RemoveCustomTabName`
    - `-AddCustomTab`
    - `-SetVisibleTabName`
    - `-SetInvisibleTabName`
    - `-SelectCustomTabName`
    - `-SelectBuiltInTab`
    - `-SelectTabIndex`
    - `-MoveSelectedTabToIndex`
    - `-SelectedTabNewName`
    - `-SelectedTabNewUrl`

#### Deprecations

- Deprecated Parameters:
    - `-CustomTabName`
    - `-CustomTabUrl`

##### Example

```PowerShell
# Add custom tab instances to client setting:
$itemA = New-CMSoftwareCenterTabItem -Name "1abc" -Url "http://www.a"
$itemB = New-CMSoftwareCenterTabItem -Name "2abc" -Url "https://www.b"
$itemC = New-CMSoftwareCenterTabItem -Name "3abc" -Url "http://www.c"
$itemD = New-CMSoftwareCenterTabItem -Name "4abc" -Url "https://www.d"
$itemE = New-CMSoftwareCenterTabItem -Name "5abc" -Url "http://www.e"
Set-CMClientSettingSoftwareCenter -DefaultSetting -AddCustomTab ($itemA, $itemB, $itemC, $itemD, $itemE)

#Set custom tab to invisible by name:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SetInvisibleTabName ("2abc","4abc", "5abc")

# Remove custom tab by name:
Set-CMClientSettingSoftwareCenter -DefaultSetting -RemoveCustomTabName ("3abc","4abc")

# Set custom tab to visible by name:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SetVisibleTabName ("2abc", "5abc")

# Move selected custom tab to specific position by name:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SelectCustomTabName "1abc" -MoveSelectedTabToIndex 0

# Move selected built-in tab to specific position:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SelectBuiltInTab AvailableSoftware -MoveSelectedTabToIndex 0

# Move selected tab to specific position by current index of position:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SelectTabIndex 0 -MoveSelectedTabToIndex 1

# Modify custom tab's name and Url by name:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SelectCustomTabName "1abc" -SelectedTabNewName "new1abc" -SelectedTabNewUrl http://www.aNew

# Clean up all custom tabs from the client setting:
Set-CMClientSettingSoftwareCenter -DefaultSetting -ClearCustomTab
```

### Set-CMComplianceRuleValue

#### Bugs that were fixed

- Failed to set remediation for registry type rule.

#### Non-breaking changes

- Modified the code to support remediation for registry type rule.

### Set-CMDistributionPoint

#### Bugs that were fixed

- Missing setting to reassign distribution point.

#### Non-breaking changes

- Added new parameter:
    - `-ReassignSiteCode`

##### Example

```PowerShell
Set-CMDistributionPoint -SiteSystemServerName "MyDP.TestDOM.net" -ReassignSiteCode "NEW" -SiteCode "OLD"
```

### Set-CMMsiDeploymentType

#### Bugs that were fixed

- The behavior wasn't consistent with the console when cmdlet changes the logon requirement settings.
- Missing application properties.
- You may specify the wrong value for `-LogonRequirementType` and `-RequireUserInteraction` when you specify `-InstallationBehaviorType InstallForSystemIfResourceIsDeviceOtherwiseInstallForUser`

#### Non-breaking changes

- Modified the validation logic for the "User Experience" settings: the "User Interaction" would be blocked only when you specified "no user logon" as the logon requirement.
- Added application properties: 'CategoryInstance_UniqueIDs' and 'Featured'
- Added combination logic to address issues in `-LogonRequirementType`, `-RequireUserInteraction`, and `-InstallationBehaviorType`

### Set-CMPackage

#### Bugs that were fixed

- Cmdlet may set oversize text in package info.

#### Non-breaking changes

- Added length validation for string values to align with console.

### Set-CMScriptDeploymentType

#### Bugs that were fixed

- Failed when specify null value to `-AddRequirement`.
- Missing application properties.

#### Non-breaking changes

- Added parameter validation for null value.
- Added application properties: 'CategoryInstance_UniqueIDs' and 'Featured'

### Set-CMSoftwareUpdateAutoDeploymentRule

#### Bugs that were fixed

- You couldn't add third-party catalogs to auto deployment rule by using this cmdlet.
- Missing Office 365 language selection.
- Missing filter options: "Architecture" and "Content Size".
- Missing validation for available and deadline time with units.
- Failed to set $false to `-EnableAfterCreate`

#### Non-breaking changes

- Added vendor support for the third-party updates.
- Added new parameter for Office 365 language selection to align with console:
    - `-O365LanguageSelection`
- Added new parameter for filter options "Architecture" and "Content Size":
    - `-Architecture`
    - `-ContentSize`
- Added validation for available and deadline time with units.
- Fixed the logic to set `-EnableAfterCreate`

##### Example

```PowerShell
# Set filter "Architecture":
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -Architecture X86, Itanium, X64 -Force  
# Set filter "Content Size":
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ ReferenceADRName  -ContentSize $size
```

### Set-CMSoftwareUpdateDeployment

#### Bugs that were fixed

- Missing option for "DelayGracePeriod".

#### Non-breaking changes

- Added new parameter for option "DelayGracePeriod":
    - `-SoftDeadlineEnabled`

### Set-CMStatusFilterRule

#### Bugs that were fixed

- `-PropertyId` failed "Exception not caught: System.ArgumentOutOfRangeException".

#### Non-breaking changes

- Added validation for Source/PropertyID/PropertyValue to avoid invalid input.

### Set-CMTaskSequenceDeployment

#### Bugs that were fixed

- Cmdlet would unexpectedly destroy object with `-InputObect`.

#### Non-breaking changes

- Fixed the object dispose issue.

### Set-CMTSStepApplyNetworkSetting

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### Set-CMTSStepApplyWindowsSettings

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### Set-CMTSStepCaptureSystemImage

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### Set-CMTSStepConnectNetworkFolder

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### Set-CMTSStepDisableBitLocker

#### Bugs that were fixed

- Need option to set "Reboot Count"

#### Non-breaking changes

- Added new parameter for "Reboot Count" option:
    - `-RebootCount`

### Set-CMTSStepEnableBitLocker

#### Bugs that were fixed

- Task sequence step with user PIN failed when task sequence running.
- Missing parameter for "Use full disk encryption" option.

#### Non-breaking changes

- Fixed security object issue.
- Added new parameter for "Use full disk encryption" option:
    - `-IsEncryptFullDisk`

### Set-CMTSStepInstallApplication

#### Bugs that were fixed

- Need option to install application step to clear its content from cache after installing the application.

#### Non-breaking changes

- Added new parameter to clear its content from cache after installing the application:
    - `-ClearCache`

### Set-CMTSStepJoinDomainWorkgroup

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### Set-CMTSStepRestoreUserState

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### Set-CMTSStepRunCommandLine

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### Set-CMTSStepRunPowerShellScript

#### Bugs that were fixed

- Task sequence step with user credential property failed to sign in when task sequence running.

#### Non-breaking changes

- Fixed security object issue.

### Set-CMWindowsFirewallPolicy

#### Bugs that were fixed

- Options shouldn't be configured when related firewall settings weren't set.

#### Non-breaking changes

- Added code to check firewall setting for dependent parameters.

### Start-CMPackageDeployment

#### Bugs that were fixed

- Cmdlet failed because of wrong property name.

#### Non-breaking changes

- Fixed property name issue.

