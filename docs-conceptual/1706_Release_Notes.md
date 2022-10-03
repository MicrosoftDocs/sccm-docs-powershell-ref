---
title: Version 1706 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 1706.
ms.date: 07/31/2017
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.author: banreetkaur
author: Banreet
manager: apoorvseth
ROBOTS: NOINDEX
---

# Configuration Manager Cmdlet Library changes for Current Branch 1706

 >[!NOTE]
 > System Center Configuration Current Branch 1702 is the baseline for these changes. See [Configuration Manager Cmdlet Library changes for Current Branch 1702](1702_release_notes.md) for more details.

## Important changes

### Documentation library updates

For the latest cmdlet library documentation, see [ConfigurationManager module reference](/powershell/module/configurationmanager/).

### Administrator console Integrated Scripting Environment (ISE) experience improvements
The script that is generated when launching ISE from the administrator console has been updated to allow for more customization and reusability. 

If a script has been previously generated, it must be removed from ```%APPDATA%\TEMP``` for the new script to be created.

### Removed cmdlets
The following cmdlets are no longer supported and have been removed:
- Add-CMComplianceRegistrySetting
- New-CMComplianceRule

## Known issues
These are known issues with the Cmdlet Library that are not resolved in this release.

### Get-CMAadConditionalAccessPolicy and Set-CMAadConditionalAccessPolicy
64-bit PowerShell environment is required for these cmdlets.

#### Workaround

- None

### New-CMWirelessProfile and Set-CMWirelessProfile
Cmdlets may fail if run in a 64-bit PowerShell environment.

#### Workaround

- Run these cmdlets in a 32-bit PowerShell environment.

### Add-CMDataWarehouseServicePoint and Set-CMDataWarehouseServicePoint
Cannot set schedule to run "Daily"

#### Workaround

- None

### Import-CMSecurityRole
Cmdlet may fail with a DirectoryNotFoundException error locating the file ```SecuredRoles.xsd```.

#### Workaround
Ensure that ```Import-Module``` is called against the ```ConfigurationManager.psd1``` file, and not the logical path or module name.

### New-CMApplicationDeployment and New-CMClientSettingDeployment
Cmdlet allows for combining the **CollectionName**, **Collection**, and **CollectionId** parameters thus causing undefined behavior.

#### Workaround
Specify only **CollectionName**, **Collection**, or **CollectionId**. Do not combine these parameters.

### Remove-CMStateMigrationPoint
Cmdlet may fail with an ArgumentOutOfRangeException when removing a State Migration Point if there is content hosted by the site role.

#### Workaround
Directly remove the state migration point from the SMS Provider.
``` powershell
$smp = Get-CMStateMigrationPoint ... # Get the state migration point
$smp.Delete() # Directly delete the object.
```

## New cmdlets
These are newly-added cmdlets for this release that add new functionality or enhance the functionality of existing cmdlets.

### Compliance settings and rules for configuration items
New cmdlets have been added to support creating settings and rules for configuration items.

- Add/Set-CMComplianceSettingActiveDirectory
- Add/Set-CMComplianceSettingAssembly
- Add/Set-CMComplianceSettingDirectory
- Add/Set-CMComplianceSettingFile
- Add/Set-CMComplianceSettingIisMetabase
- Add/Set-CMComplianceSettingRegistryKey
- Add/Set-CMComplianceSettingRegistryKeyValue
- Add/Set-CMComplianceSettingRule
- Add/Set-CMComplianceSettingScript
- Add/Set-CMComplianceSettingSqlQuery
- Add/Set-CMComplianceSettingWqlQuery
- Add/Set-CMComplianceSettingXPathQuery
- Get-CMComplianceRule
- Get-CMComplianceSetting
- New-CMComplianceRuleAssembly
- New-CMComplianceRuleExistential
- New-CMComplianceRuleFileFolderAttribute
- New-CMComplianceRuleFileFolderDate
- New-CMComplianceRuleFileFolderPermission
- New-CMComplianceRuleFileFolderSimple
- New-CMComplianceRuleFileFolderSize
- New-CMComplianceRuleRegistryKeyPermission
- New-CMComplianceRuleValue
- New-CMComplianceRuleVersion
- Remove-CMComplianceRule
- Remove-CMComplianceSetting

#### Example 1: Create a registry key value setting with no rules
``` powershell
# Creates a setting looking for HKLM\Software\Microsoft\Windows NT\CurrentVersion:ReleaseId
$ci | Add-CMComplianceSettingRegistryKeyValue -SettingName "ReleaseId no rule" -DataType String -Hive LocalMachine -KeyName "SOFTWARE\Microsoft\Windows NT\CurrentVersion" -ValueName "ReleaseId" -NoRule
```

#### Example 2: Create a registry key value setting with an existential rule
``` powershell
# Creates a setting requiring the HKLM\Software\Microsoft\WindowsNT\CurrentVersion:ReleaseId registry key to exist
$ci | Add-CMComplianceSettingRegistryKeyValue -SettingName "ReleaseId must exist" -DataType String -Hive LocalMachine -KeyName "SOFTWARE\Microsoft\Windows NT\CurrentVersion" -ValueName "ReleaseId" -ExistentialRule -Existence MustExist
```

#### Example 3: Create a registry key value setting with a value rule
``` powershell
# Creates a setting requiring the HKLM\Software\Microsoft\WindowsNT\CurrentVersion:ReleaseId registry key to be equal to "1703"
$ci | Add-CMComplianceSettingRegistryKeyValue -SettingName "ReleaseId must be 1703" -DataType String -Hive LocalMachine -KeyName "SOFTWARE\Microsoft\Windows NT\CurrentVersion" -ValueName "ReleaseId" -ValueRule -ExpressionOperator IsEqual -ExpectedValue "1703"
```

#### Example 4: Create a file rule that requires the file to have a specific attribute set
``` powershell
$ci | Add-CMComplianceSettingFile -Path "C:\" -FileName "hiberfile.sys" -NoRule -SettingName "hiberfile.sys must have system attribute"
$setting = $ci | Get-CMComplianceSetting -SettingName "hiberfile.sys must have system attribute" # Get the SDK setting object
$rule = $setting | New-CMComplianceRuleFileFolderAttribute -RuleName "hiberfile.sys must be system" -System $true # Create the rule
$ci | Add-CMComplianceSettingRule $rule # Bind the rule to the CI
```

### Updates and servicing
New cmdlets have been added to support automating updates and servicing in Configuration Manager.

- Enable-CMSiteFeature
- Get-CMSiteFeature
- Get-CMSiteUpdate
- Get-CMSiteUpdateHistory
- Get-CMSiteUpdateInstallStatus
- Install-CMSiteUpdate
- Invoke-CMSitePromotePreproductionClient
- Invoke-CMSiteUpdateCheck
- Invoke-CMSiteUpdateDownload
- Invoke-CMSiteUpdatePrerequisiteCheck

#### Example 1: Download an update and monitor its status
``` powershell
# Get the update object for the 1706 TP and invoke a download
$update = Get-CMSiteUpdate -Name "Configuration Manager Technical Preview 1706" -Fast
$update | Invoke-CMSiteUpdateDownload
``` powershell

# Now monitor the download status
``` powershell
while($true) {
    cls
    $update | Get-CMSiteUpdateInstallStatus  -Step Download | select orderid, progress, description | ft
    sleep 5
}
```

#### Example 2: Install an update and monitor its status
``` powershell
$update = Get-CMSiteUpdate -Name "Configuration Manager Technical Preview 1706" -Fast
$update | Install-CMSiteUpdate -IgnorePrerequisiteWarning -Force

while($true) {
    cls
    $update | Get-CMSiteUpdateInstallStatus -Step All -Complete | select orderid, progress, description -Last 10 | ft
    sleep 5
}
```

### Enhanced detection methods for deployment types
New cmdlets have been added to support adding enhanced detection methods to Windows Installer (MSI), Script, and Mac deployment types.

- Windows Installer & Script detection clauses
    - New-CMDetectionClauseDirectory
    - New-CMDetectionClauseFile
    - New-CMDetectionClauseRegistryKey
    - New-CMDetectionClauseRegistryKeyValue
    - New-CMDetectionClauseWindowsInstaller
- Mac detection clauses
    - New-CMDetectionClauseMacBundle
    - New-CMDetectionClauseMacPackage

#### Example: Add a detection clause requiring a specific product ID and directory name to be present for a Windows Installer deployment type.
``` powershell
$clause1 = New-CMDetectionClauseWindowsInstaller -ProductCode $guid [Value -ExpressionOperator IsEquals -ExpectedValue "1.1.1.1" # Do a version check
$clause2 = New-CMDetectionClauseDirectory -DirectoryName "mymsi" -Path "C:\" -Existence # c:\mymsi should exist
$app | Add-CMMsiDeploymentType -ContentLocation "\\myserver\mypath\mymsi.msi" -Force -AddDetectionClause ($clause1, $clause2)
```

#### Notes
It is not currently supported to modify detection clauses in place. 

It is not currently supported to group or ungroup detection clauses.

### Task sequences
New cmdlets have been added to support modifying task sequence steps and groupings.

- Task sequence groups and steps
    - Get/New/Remove/Set-CMTaskSequenceGroup    
    - Add/Get/Remove-CMTaskSequenceStep
- Task sequence conditions (Get and New verbs supported)
    - CMTaskSequenceStepConditionIfStatement
    - CMTaskSequenceStepConditionQueryWmi
    - CMTaskSequenceStepConditionRegistry
    - CMTaskSequenceStepConditionFile
    - CMTaskSequenceStepConditionFolder
    - CMTaskSequenceStepConditionOperatingSystem
    - CMTaskSequenceStepConditionSoftware
- Task sequence commands (Get, New, Remove, and Set verbs supported)
    - CMTaskSequenceStepRunCommandLine
    - CMTaskSequenceStepInstallApplication
    - CMTaskSequenceStepInstallSoftware
    - CMTaskSequenceStepInstallUpdate
    - CMTaskSequenceStepPartitionDisk        
    - CMTaskSequenceStepReboot
    - CMTaskSequenceStepRunPowerShellScript
    - CMTaskSequenceStepSetupWindowsAndConfigMgr
    - CMTaskSequenceStepSetVariable
- Task sequence support commands
    - New-CMTaskSequencePartitionSetting

#### Example: Create a custom task sequence that runs two PowerShell scripts
``` powershell
$step1 = New-CMTaskSequenceStepRunPowerShellScript -Name "Run script 1" -PackageID $PackageId -ScriptName "script1.ps1" -ExecutionPolicy Bypass
$step2 = New-CMTaskSequenceStepRunPowerShellScript -Name "Run script 2" -PackageID $PackageId -ScriptName "script2.ps1" -ExecutionPolicy Bypass
$ts = New-CMTaskSequence -Name "Run scripts" -CustomTaskSequence
$ts | Add-CMTaskSequenceStep -Step ($step1, $step2)
```

#### Note
Additional task sequence commands to be added in a future release.

### iOS Bulk Enrollment
New cmdlets have been added to support iOS bulk enrollment scenarios.

- Get-CMCorpOwnedDevice
- Get-CMIosEnrollmentProfile
- New-CMIosEnrollmentProfile
- Remove-CMCorpOwnedDevice
- Remove-CMIosEnrollmentProfile
- Set-CMIosEnrollmentProfileAssignment

### Wireless profiles
New cmdlets have been added to support wireless profiles.
- Get-CMWirelessProfile
- New-CMWirelessProfile
- Remove-CMWirelessProfile
- Set-CMWirelessProfile

### Deployment cmdlets
New cmdlets have been added to support additional deployment scenarios.
- New-CMClientSettingsDeployment 
    - Supersedes ```Start-CMClientSettingsDeployment```
- New-CMApplicationDeploymentSimulation 
    - Supersedes ```Start-CMApplicationDeploymentSimulation```

### Resource tracking and recovery (BETA)
New cmdlets have been added to support tracking SMS Provider objects used by the PowerShell runtime, and to clean up these resources when they are no longer needed.

- Disconnect-CMTrackedObject
- Start-CMObjectTracking
- Stop-CMObjectTracking

When ```Start-CMObjectTracking``` is run, the PowerShell runtime will track ```IResultObject``` objects created by Cmdlet Library cmdlets. Cmdlets that are not manually cleaned up with ```.Dispose()``` can be reclaimed by using ```Disconnect-CMTrackedObject``` against an individual object (example: ```$o | Disconnect-CMTrackedObject```), or ```Disconnect-CMTrackedObject -All``` can be used reclaim _all_ tracked objects. 

Note that once an object is reclaimed, it can no longer be reused or passed to another cmdlet through the object pipeline. 

```Stop-CMObjectTracking``` can be used to turn off object tracking. Note that previously allocated objects will remain active.

Unclaimed resources can cause Quota Violation errors to be raised by the SMS Provider. These issues typically manifest from working with very large sets of SMS Provider objects or in very long running environments

#### Notes
This is an experimental feature and may be subject to change or removal in a future release. This feature is opt-in and is not enabled by default.

### Get-CMClientHealthSummary
This cmdlet can be used to get client health information for a collection with an optional date range.

#### Example: Gets client health for "All Systems" starting in January, 2017.
``` powershell
Get-CMCollection -Name "All Systems" | Get-CMClientHealthSummary -StartDate "2017/01/01"
```
### Get-CMSoftwareUpdateSyncStatus
This cmdlet can be used to get the status of a synchronization with Windows Update.

### Invoke-CMContentRedistribution
This cmdlet can be used to redistribute content that has already been deployed to a distribution point. This supports application, package, boot image, software update, driver, image, task sequence, and operating system content distributions.

#### Example: Redistribute a package to a distribution point
``` powershell
Get-CMPackage -Name Contoso | Invoke-CMContentRedistribution -DistributionPointName myserver.contoso.com
```

### Invoke-CMDeploymentSummarization
This cmdlet can be used to immediately perform deployment summarization.

### Stop-CMMigrationSource
This cmdlet can be used to stop a site migration from occurring. ```Sync-CMMigrationSource``` must be used to resume migration.

## Cmdlet changes
The following changes have been made to existing cmdlets for this release. Changes may be new functionality, bug fixes, or deprecations, and may be breaking. If you use one of the cmdlets or feature areas listed in this section, please carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

### Add-CMApplicationCatalogWebsitePoint
#### Bugs that were fixed
Cmdlet may fail with a KeyNotFoundException error if the value specified for **ApplicationWebServicePointServer** does not contain the expected site role.
#### Non-breaking changes
Added **ApplicationWebServicePointServer** to allow for defining a web service point by using the output of ```Get-CMApplicatinWebServicePoint```. Cannot be combined with **ApplicationWebServicePointServerName**.

### Add-CMAssetIntelligenceSynchronizationPoint
#### Bugs that were fixed
If an invalid **CertificatePath** is specified, role may created incorrectly. See also: [Remove-CMAssetIntelligenceSynchronizationPoint](#remove-cmassetintelligencesynchronizationpoint).

### Add-CMDataWarehouseServicePoint
#### Breaking changes
**DaysOfWeek** value changed from an integer to ```DataWarehouseDaysOfWeek``` enum value.
#### Bugs that were fixed
**DataWarehouseDatabaseServerName** does not validate FQDN hostname is less than 16 characters.
#### Non-breaking changes
Added **DataWarehouseInstanceName** parameter to support specifying a SQL Server instance.

### Add-CMMacDeploymentType
#### Non-breaking changes
Added **AddDetectionClause** parameter to support adding detection clauses to the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

### Add-CMMsiDeploymentType
#### Non-breaking changes
Added **AddDetectionClause** parameter to support adding detection clauses to the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

Added **RebootBehavior** parameter to allow for defining reboot behavior.

### Add-CMScriptDeploymentType
#### Non-breaking changes
Added **AddDetectionClause** parameter to support adding detection clauses to the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

Added **RebootBehavior** parameter to allow for defining reboot behavior.

### Add-CMWindowsPhoneStoreDeploymentType
#### Bugs that were fixed
Invalid deployment type may be created if windowsphone.com URL is specified.

### Approve-CMApprovalRequest and Deny-CMApprovalRequest
#### Non-breaking changes
Cmdlet now supports approving or denying an approval request by using the GUID associated with the request.

### Get-CMAlert
#### Bugs that were fixed
Alert types related to Endpoint Protection or Client Health are not retrieved by the cmdlet.

### Get-CMApprovalRequest
#### Non-breaking changes
Added **CurrentState** parameter to allow for filtering approval requests by their approval state.

### Get-CMMaintenanceWindow
#### Bugs that were fixed
Cmdlet may fail with a NullReferenceException if there are no maintenance windows defined for the site.

### Import-CMWirelessProfileConfigurationItem
#### Bugs that were fixed
**Path** parameter does not validate that input is a valid UNC path.

### Import-CMClientCertificatePfx
#### Non-breaking changes
Added **ForSmimeEncryption** parameter to indicate that Microsoft Intune can use the certificate for device encryption.

### Import-CMDriver
#### Bugs that were fixed
**Path** parameter does not validate that the input is a valid UNC path.

### Import-CMTaskSequence
#### Bugs that were fixed
**ImportFilePath** parameter does not validate that the input is a valid UNC path.

### Lock-CMObject
#### Bugs that were fixed
Cmdlet may fail with a NullReferenceException if invoked against an object that does not support locking.

### New-CMADGroupDiscoveryScope
#### Bugs that were fixed
**GroupDN** parameter does not validate that the input is a valid distinguished name.

### New-CMAlertSubscription
#### Bugs that were fixed
If more than one value is specified for **EmailAddress**, the subscription is incorrectly configured.

### New-CMApplicationDeployment
#### Non-breaking changes
Added **EnableSoftDeadline** parameter to configure delayed enforcement.

### New-CMCertificateProfileScep
#### Non-breaking changes
**KeySize** parameter now allows for a value of ```4096``` bytes.

### New-CMTaskSequence
#### Non-breaking changes
Added **TimeZone** parameter allowing for specifying time zone information when using **InstallOperatingSystemImage**. The time zone can be specified by using the ```Get-TimeZone``` cmdlet.

### New-CMSoftwareUpdateAutoDeploymentRule
#### Bugs that were fixed
If **Language** is specified, an invalid auto deployment rule may be created.

If **Location** does not exist, an invalid auto deployment rule may be created.

### Remove-CMAssetIntelligenceSynchronizationPoint
#### Bugs that were fixed
Cmdlet may fail with an ArgumentNullException if removing an incorrectly configured asset intelligence synchronization point role.

### Remove-CMMaintenanceWindow
#### Bugs that were fixed
**WhatIf** or **Confirm** may cause cmdlet to return an ItemNotFoundException error.

<!-- This is currently not working correctly. -->
<!--
### Remove-CMStateMigrationPoint
#### Breaking changes
Cmdlet will now ask for confirmation if there is existing user state that has not been restored. **Force** will prevent this from occurring.
-->

### Remove-CMUpdateGroupDeployment
#### Bugs that were fixed
Cmdlet may fail to remove a valid deployment with an ItemNotFoundException error.

### Remove-CMUserCollectionDirectMembershipRule
#### Non-breaking changes
**ResourceName** parameter now supports wildcard values.

<!--
### Set-CMAntimalwarePolicy
#### Bugs that were fixed
Cannot specify a **FallbackOrder** of ```None```.
-->

### Set-CMAlertSubscription
#### Deprecations
**EmailAddress** parameter has been superseded by **AddEmailAddress** and **RemoveEmailAddress**

#### Non-breaking changes
Added **AddEmailAddress** parameter to allow for modifying e-mail addresses in place. Cannot combine with **EmailAddress**.

Added **RemoveEmailAddress** parameter to allow for removing e-mail addresses in place. Cannot combine with **EmailAddress**.

### Set-CMApplicationDeployment
#### Non-breaking changes
Added **EnableSoftDeadline** parameter to configure delayed enforcement.

### Set-CMConfigurationPolicyDeployment
#### Bugs that were fixed
Cmdlet may fail to deploy a remote connection profile.
#### Non-breaking changes
Added **RemoteConnectionProfileName** and **RemoteConnectionProfileId** parameters to allow for deploying a remote connection profile by name or ID.

### Set-CMDataWarehouseServicePoint
#### Breaking changes
**DaysOfWeek** value changed from an integer to ```DataWarehouseDaysOfWeek``` enum value.

#### Bugs that were fixed
Unused parameters may cause values to be reset to defaults when the cmdlet is run.

**DataWarehouseDatabaseServerName** does not validate FQDN hostname is less than 16 characters.
#### Non-breaking changes
Added **DataWarehouseInstanceName** parameter to support specifying a SQL Server instance.

### Set-CMEmailNotificationComponent
#### Bugs that were fixed
If **UseSsl** is specified without specifying a value for **Port**, the SMTP ports may not be properly configured.

### Set-CMHierarchySetting
#### Bugs that were fixed
Cmdlet allows for setting an exclusion collection to be a built-in collection (such as All Systems).

#### Non-breaking changes
Added **EnablePrereleaseFeature** parameter to support enabling prerelease features. This is a one-time change and will prompt for confirmation unless **Force** is used. See [updates & servicing](#updates-and-servicing) for more details.

### Set-CMMacDeploymentType
#### Non-breaking changes
Added **AddDetectionClause** parameter to support adding detection clauses to the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

Added **RemoveDetectionClause** parameter to support removing detection clauses from the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

### Set-CMMsiDeploymentType
#### Non-breaking changes
Added **AddDetectionClause** parameter to support adding detection clauses to the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

Added **RemoveDetectionClause** parameter to support removing detection clauses from the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

Added **RebootBehavior** parameter to allow for defining reboot behavior.

### Set-CMProgram
#### Bugs that were fixed
**ProgramRunType** changes may not be applied to the specified program.

### Set-CMScriptDeploymentType
#### Non-breaking changes
Added **AddDetectionClause** parameter to support adding detection clauses to the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

Added **RemoveDetectionClause** parameter to support removing detection clauses from the deployment type. See [enhanced detection methods section](#enhanced-detection-methods-for-deployment-types) for more information.

Added **RebootBehavior** parameter to allow for defining reboot behavior.

### Set-CMSiteMaintenanceTask
#### Bugs that were fixed
Cannot enable alerts for tasks related to site backups.

### Set-CMSoftwareInventory
#### Breaking changes
**Tag1Id**, **Tag2Id**, and **Tag3Id** parameters now perform validation to ensure correct formatting is used.

#### Non-breaking changes
Added **PassThru** parameter support.

#### Bugs that were fixed
Specifying an invalid **Tag2Id** value may cause the originally specified tag to be removed.

### Set-CMSoftwareUpdateAutoDeploymentRule
#### Bugs that were fixed
If **Location** does not exist, an invalid auto deployment rule may be created.

### Set-CMSoftwareUpdatePointComponent
#### Non-breaking changes
Added **ContentFileOption** parameter to configure Windows 10 update behavior.

### Set-CMWindowsPhoneStoreDeploymentType
#### Bugs that were fixed
Invalid deployment type may be created if windowsphone.com URL is specified.