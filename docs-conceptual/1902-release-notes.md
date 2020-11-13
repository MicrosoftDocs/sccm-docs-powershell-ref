---
title: Version 1902 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 1902. 
ms.date: 03/27/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
ROBOTS: NOINDEX
---

# Configuration Manager Cmdlet Library changes for version 1902

*Applies to: Configuration Manager (Current Branch)*

> [!NOTE]  
> Configuration Manager current branch version 1810 is the baseline for these changes. For more information, see [Configuration Manager Cmdlet Library changes for version 1810](https://docs.microsoft.com/powershell/sccm/1810-release-notes).


## Important changes

### New cmdlets

#### Get-CMBoundaryGroupSiteSystem
Use this cmdlet to get site system in specified boundary group.

```PowerShell
Get-CMBoundaryGroupSiteSystem -Id $boundaryGroup.GroupID 
```

#### Get-CMDistributionPointDriveInfo
Use this cmdlet to get distribution point drive info.

```PowerShell
$dp = Get-CMDistributionPoint -SiteSystemServerName $ReferenceSiteSystemServerName 
$dp | Get-CMDistributionPointDriveInfo     
```

#### Invoke-CMAnalyzePackage
Use this cmdlet to analyze a specific package.

```PowerShell
Invoke-CMAnalyzePackage -PackageName $packageName 
```


#### Invoke-CMConvertPackage
Use this cmdlet to convert a specific package to an application.

```PowerShell
Invoke-CMConvertPackage -PackageName $packageName
```

#### New-CMScript
Use this cmdlet to create a new PowerShell script. It only supports scripts that don't contain any parameter.

```PowerShell
New-CMScript -ScriptName "CMScript" -ScriptText 'Write-Host "New Script"'
New-CMScript -ScriptName "ImportScript" -ScriptFile \\abc\importedscript.ps1
```

#### Set-CMClientSettingDeliveryOptimization
Use this cmdlet to set client settings for the Delivery Optimization feature.

```PowerShell
[Default] Set-CMClientSettingDeliveryOptimization -DefaultSetting -Enable $true
[Customized] Set-CMClientSettingDeliveryOptimization -Name $ReferenceClientDeviceSettingName -Enable $true
```

#### Set-CMClientSettingWindowsAnalytics
Use this cmdlet to set client settings for the Windows Analytics feature.

```PowerShell
[Default] Set-CMClientSettingWindowsAnalytics -DefaultSetting -Enable $true -CommercialIdKey $commercialIdKey -Win10Telemetry EnhancedLimited -EnableEarlierTelemetry $true -IEDataCollectionOption AllZones
[Customized] Set-CMClientSettingWindowsAnalytics -Name $ReferenceClientDeviceSettingName -Enable $true -CommercialIdKey $commercialIdKey -Win10Telemetry EnhancedLimited -EnableEarlierTelemetry $true -IEDataCollectionOption AllZones
```

### Removed cmdlets
None

### Deprecated cmdlets
None



## Known issues

The following items are known issues with the Cmdlet Library that aren't resolved in this version.


### Get-CMAadConditionalAccessPolicy and Set-CMAadConditionalAccessPolicy

These cmdlets require a 64-bit PowerShell environment.

#### Workaround
- None


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

- Disconnect-CMObject
- Start-CMObjectTracking
- Stop-CMObjectTracking

When you run `Start-CMObjectTracking`, the PowerShell runtime tracks `IResultObject` objects created by Cmdlet Library cmdlets. For cmdlets that aren't manually cleaned up with `.Dispose()`, reclaim them by using `Disconnect-CMObject` against an individual object.

#### Example
```powershell
# Reclaim a single tracked object
$o | Disconnect-CMObject

# Reclaim all tracked objects
Disconnect-CMObject -All
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


### Add-CMDeviceAffinityToUser
#### Bugs that were fixed
- Add/Remove-CMDeviceAffinityToUser -UserId/-UserName need use "-DeviceId/-DeviceName" together.
#### Non-breaking changes
- Added parameter check for -DeviceID and -DeviceName, user should specify at least one of them.

### Add-CMDeviceCollectionDirectMembershipRule
#### Bugs that were fixed
- When same resource is added to same collection using 'Add-CMDeviceCollectionDirectMembershipRule ' command in PowerShell, it shows a blank warning "WARNING: " and doesn't give error "An object with the specified name already exists".
#### Non-breaking changes
- Added a missing resource.

### Add-CMDistributionPoint
#### Non-breaking changes
- Added "-EnableLedbat" parameter to enable/disable LEDBAT on DP

### Add-CMScriptDeploymentType
#### Bugs that were fixed
- Add-CMScriptDeploymentType not align with UI by default
#### Non-breaking changes
- Modified the initialization code to align with UI (Estimated installation time = 0, logon requirement=only when a user is logged on).

### Approve-CMApprovalRequest
#### Non-breaking changes
- Added new parameter InstallActionBehavior (has two options: InstallNow, InstallNonBusinessHours), admin can specify whether to install application right away after it is approved or install during non-business hours. It is an optional parameter and by default it's equal to "InstallNow". 

### Get-CMDevice
#### Bugs that were fixed
- Get-CMDevice is missing SMSAssignedSites property - this was available pre-1806. 
#### Non-breaking changes
- Added two new switch parameters to allow customer specify the class of the output:
    - -ReturnCollectionMember: will force return instance of sms collection member class
    - -ReturnResource: will force return instance of SMS_Resource class.

    If you use default parameter without ReturnCollectionMember/ReturnResource, then the behavior would be same as 1802/1810: the returned instance could be in different classes with different specified parameters.

### Get-CMPackage
#### Bugs that were fixed
- Get-CMPackage needs a -Fast switch
#### Non-breaking changes
- Added parameter -Fast to support fast query.

### Import-CMDriver
#### Bugs that were fixed
- Set-CMDriver -SupportedPlatformName will fail for arrays
#### Non-breaking changes
- Fixed array value issue for SupportPlatformName parameter.

### Invoke-CMScript
#### Bugs that were fixed
- Invoke-CMScript cmdlet is expecting an object that can't be obtained.
#### Non-breaking changes
- Corrected the type validation.

### New-CMActiveDirectoryForest
#### Bugs that were fixed
- Creating Active Directory Forest - User does not work via Powershell, only if created through the GUI.
#### Non-breaking changes
- Imported the account to global account after user set the credential.
- Added new parameter -Password for creating credential with password.

### New-CMApplication
#### Bugs that were fixed
- User can't specify a blank Owner or SupportContact parameter with the New-CMApplication cmdlet
#### Non-breaking changes
- Allow $null for Owner/SupportContact when creating new application, the default value would be current user.
- Added new parameters for Owner/SupportContact to support array input.

### New-CMApplicationDeployment
#### Non-breaking changes
- Added new parameter ReplaceToastNotificationWithDialog (Boolean), admin can specify whether to replace toast notifications with dialog when required software becomes available on the client machine. It is an optional parameter and false by default. 

### New-CMCoManagementPolicy
#### Non-breaking changes
- Added support for new workloads (DCWorkloadEnabled, O365WorkloadEnabled, ClientAppsWorkloadEnabled).


### New-CMDetectionClauseWindowsInstaller
#### Bugs that were fixed
- Add/Set-CMMsiDeploymentType -AddDetectionClause failed "Invalid expression: either datatype of operand doesn't match or the operator is invalid for the datatype".
#### Non-breaking changes
- Modified the logic of the datatype initialization to make sure it's correct when you specify the Existence switch.

### New-CMOperatingSystemImageUpdateSchedule
#### Non-breaking changes
- New parameter added to match changes made to create schedule wizard in UI: 
    - -RemoveSupersededUpdates

### New-CMOperatingSystemUpgradeUpdateSchedule
#### Non-breaking changes
- New parameter added to match changes made to create schedule wizard in UI: 
    - -RemoveSupersededUpdates

### New-CMPackageDeployment
#### Bugs that were fixed
- New-CMPackageDeployment has inconsistent warnings
#### Non-breaking changes
- Modified the default behavior of the SlowNetwork option to align with UI.

### New-CMStatusFilterRule
#### Bugs that were fixed
- New-CMStatusFilterRule does not work as expected
- Unable to create a new Status Filter Rule with Property "Package ID.
#### Non-breaking changes
- Added more condition for property ID/value check to unblock case without -PropertyID specified.
- Added logic to allow user set property id = 'Package ID' when the source is 'Client'.

### New-CMTaskSequenceDeployment
#### Bugs that were fixed
- Unable to set expiration time of a task sequence deployment
- New-CMTaskSequenceDeployment , $result cannot get the object from this cmdlet.
#### Non-breaking changes
- Added alias "DeploymentExpireDateTime" to parameter -DeadlineDateTime to align with Set- cmdlet.
- Removed the using block, the deployment object should not be disposed.

### New-CMTaskSequenceMedia
#### Non-breaking changes
- A new parameter added to match the changes added to task sequence media creation UI: 
    - -TemporaryFolder (alias "TemporaryDirectory", "StagingArea")

### New-CMTSStepRunPowerShellScript
#### Breaking changes
- Parameter sets added: RunScriptFromSource, RunScriptFromPackage.
- PackageID and PackageName parameters are no longer mandatory because users can alternatively enter new parameter SourceScript
#### Non-breaking changes
- New parameters added to match changes made to Run Power Shell script step in task sequence editor UI: 
    - -SourceCode
    - -WorkingDirectory
    - -OutputVariableName
    - -TimeOut
    - -UserName
    - -Password
    - -SuccessCodes

### Remove-CMDeviceAffinityFromUser
#### Bugs that were fixed
- Add/Remove-CMDeviceAffinityToUser -UserId/-UserName need use "-DeviceId/-DeviceName" together.
#### Non-breaking changes
- Added parameter check for -DeviceID and -DeviceName, user should specify at least one of them.

### Set-CMActiveDirectoryForest
#### Bugs that were fixed
- Creating Active Directory Forest - User does not work via Powershell, only if created through the GUI.
#### Non-breaking changes
- Imported the account to global account after user set the credential.
- Added new parameter -Password for creating credential with password.

### Set-CMApplicationDeployment
#### Non-breaking changes
- Added new parameter ReplaceToastNotificationWithDialog (Boolean), admin can specify whether to replace toast notifications with dialog when required software becomes available on the client machine. It is an optional parameter and false by default. 

### Set-CMClientSetting
#### Non-breaking changes
- Added new parameter ReplaceToastNotificationWithDialog (Boolean), admin can specify whether to replace toast notifications with dialog when machine requires restart. It is an optional parameter and false by default. 

### Set-CMClientSettingComputerRestart
#### Non-breaking changes
- Added new parameter ReplaceToastNotificationWithDialog (Boolean), admin can specify whether to replace toast notifications with dialog when machine requires restart. It is an optional parameter and false by default. 

### Set-CMComplianceRuleExistential
#### Bugs that were fixed
- Set-CMComplianceRuleExistential -Rule does not work to set rule value.
- Set-CMComplianceRuleExistential -ExpectedValue don`t allow set to negative number, without select parameter [-Existence Occurs] it set successfully.
#### Non-breaking changes
- Modified the WarnIgnoredParameter function to make sure it would call IsBoundParameterUsed with parameter silent='true' to avoid blocking error when child cmdlet overrides base parameter as non-public parameter.
- Moved validation for the expected result to a common place.

### Set-CMDiscoveryMethod
#### Bugs that were fixed
- Set-CMDiscoveryMethod does not have a parameter to configure the discovery account.
#### Non-breaking changes
- Added new parameter -UserName to specify discovery account for new adding ADContainer for AD System/User Discovery.

### Set-CMDistributionPoint
#### Non-breaking changes
- Added "-EnableLedbat" parameter to enable/disable LEDBAT on DP


### Set-CMDriver
#### Bugs that were fixed
- Set-CMDriver -SupportedPlatformName will fail for arrays
#### Non-breaking changes
- Fixed array value issue for SupportPlatformName parameter.
- Added new parameters for SupportedPlatform: -AddSupportedPlatformName; -RemoveSupportedPlatformName; -ClearSupportedPlatform
#### Deprecations
- Deprecated parameter: -SupportedPlatformName

### Set-CMManagementPoint
#### Breaking changes
- Modified the parameter validation to align with UI, added code to reset client connection type when enable/disable cloud gateway. It's a breaking change since we would block user to enable cloud gateway (-EnableCloudGateway) without SSL.
#### Bugs that were fixed
- Set-CMManagementPoint -EnableCloudGateway, at first set MP as HTTPS / EnableCloudGateway true, then set MP to HTTP the EnableCloudGateway should not be check.

### Set-CMStatusFilterRule
#### Bugs that were fixed
- Set-CMStatusFilterRule doesn't work with setting Package ID
#### Non-breaking changes
- Allow user to set property without specify source again, the different with UI is that we need user to specify -PropertyID and -PropertyValue together.
- Added code to avoid empty warning message when object does not exist.

### Set-CMTSStepRunPowerShellScript
#### Non-breaking changes
- New parameters added to match changes made to Run Power Shell script step in task sequence editor UI: 
    - -SourceCode 
    - -WorkingDirectory 
    - -OutputVariableName 
    - -TimeOut 
    - -UserName
    - -Password 
    - -SuccessCodes

### Set-CMWindowsFirewallPolicy
#### Bugs that were fixed
- Set/Remove-CMWindowsFirewallPolicy  -InputObject need to input correct type from New-CMWindowsFirewallPolicy.
#### Non-breaking changes
- Corrected the type validation.



## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To submit bug reports, use [send a smile in the Configuration Manager console](https://docs.microsoft.com/sccm/core/understand/find-help#product-feedback). For new feature requests, use [UserVoice](https://configurationmanager.uservoice.com).



