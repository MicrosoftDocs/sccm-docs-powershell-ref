# System Center Configuration Manager Cmdlet Library changes for Current Branch 1802

>[!NOTE]
> System Center Configuration Current Branch 1710 is the baseline for these changes. For more information, see [System Center Configuration Manager Cmdlet Library changes for Current Branch 1710](https://docs.microsoft.com/powershell/sccm/1710_release_notes).

## Important changes
### Administrator console no longer creates hard link for PowerShell module
The administrator console installer has been updated to allow for importing the ConfigurationManager module by logical name without using a hard link from ```<installdir>\bin\ConfigurationManager``` to ```<installdir>\bin```.

### Deprecated cmdlets
- ```New-CMGlobalCondition``` and ```Set-CMGlobalCondition``` have been superseded by the [new family of global condition cmdlets](#gccmdlets).

### Disable PSDrive auto-creation
When the ConfigurationManager.psd1 module is loaded, PowerShell automatically tries to create a connection to the last SMS Provider that was accessed using the Configuration Manager console. In some scenarios, this connection behavior may not be desirable. A per-user registry key has been added that can disable this behavior and require manual drive creation. To configure the behavior, use the registry key: ```HKEY_CURRENT_USER\Software\Microsoft\ConfigMgr10\PowerShell``` and set the value ```DisableCMDriveAutoCreate``` to a DWORD of 1 (drive auto-creation is disabled) or 0 (default behavior). Deleting ```DisableCMDriveAutoCreate``` also enables default behavior.

> [!NOTE]
> When drive auto-creation is disabled, the Configuration Manager console may report an error when launching a PowerShell window.

## How to provide feedback or report issues
Many of the fixes and improvements described in this document are a result of customer feedback.

To leave bug reports, use the [Feedback Hub](https://docs.microsoft.com/sccm/core/understand/find-help). For feature requests, use [UserVoice](https://configurationmanager.uservoice.com).

## Known issues
The following items are known issues with the Cmdlet Library that are not resolved in this release.

### New-CMCloudDistributionPoint
Cmdlet is currently non-functional.

#### Workaround
- None

### Get-CMAadConditionalAccessPolicy and Set-CMAadConditionalAccessPolicy
64-bit PowerShell environment is required for these cmdlets.

#### Workaround
- None

### Import-CMSecurityRole
Cmdlet may fail with a DirectoryNotFoundException error locating the file ```SecuredRoles.xsd```.

#### Workaround
- Make sure that ```Import-Module``` is called against the ```ConfigurationManager.psd1``` file, and not the logical path or module name.

### Set-CMSoftwareUpdatePoint
Changes to **Schedule** may not be shown in the Configuration Manager console even though the underlying SMS Provider object has been changed.

#### Workaround
- Quit and relaunch the Configuration Manager console.

## New cmdlets
The following items are newly added cmdlets for this release that add new functionality or enhance the functionality of existing cmdlets.

### Co-Management cmdlets
```New-CMCoManagementPolicy``` will allow for creation of a co-management policy.

### <a name="gccmdlets"></a>Global condition cmdlets
New cmdlets have been added to support creating and modifying global conditions. New, and Set verbs are supported.
- CMGlobalConditionActiveDirectoryQuery
- CMGlobalConditionAssembly
- CMGlobalConditionFile
- CMGlobalConditionIisMetabase
- CMGlobalConditionRegistryKey
- CMGlobalConditionRegistryValue
- CMGlobalConditionScript
- CMGlobalConditionSqlQuery
- CMGlobalConditionWqlQuery
- CMGlobalConditionXPathQuery
- CMGlobalConditionOmaUri

### Task Sequence cmdlets
New cmdlets have been added to support modifying task sequence steps.
- Task sequence commands (Get, New, Remove, and Set verbs supported)
    - CMTSCaptureNetworkSettings
    - CMTSCaptureSystemImage
    - CMTSCaptureUserState
    - CMTSCaptureWindowsSetting
    - CMTSConvertDisk
    - CMTSDisableBitLocker
    - CMTSEnableBitLocker
    - CMTSPrepareSmsClient
    - CMTSPrepareWindows
    - CMTSStepApplyDataImage
    - CMTSStepDownloadPackageContent
    - CMTSStepJoinDomainWorkgroup
    - CMTSStepOfflineEnableBitLocker
    - CMTSStepPrestartCheckAction
    - CMTSStepRestoreUserState
    - CMTSStepUpgradeOperatingSystem

- Task sequence condition commands
    - ```New-CMTSStepConditionOperatingSystemLanguage``` cmdlet for creation of an operating system language condition.

- Task sequence copying cmdlets
    - ```Copy-CMTaskSequence``` cmdlet for creating a copy of an existing task sequence.

### Convert-CMDeploymentType
This cmdlet allows for getting a native ```DeploymentType``` object from an ```SMS_DeploymentType``` WMI object instance. Can be combined with ```Get-CMDeploymentType```.

### Resource tracking and recovery (BETA)
New cmdlets have been added to support tracking SMS Provider objects used by the PowerShell runtime, and to clean up these resources when they're no longer needed.

- Disconnect-CMObject
- Start-CMObjectTracking
- Stop-CMObjectTracking

When ```Start-CMObjectTracking``` is run, the PowerShell runtime will track ```IResultObject``` objects created by Cmdlet Library cmdlets. Cmdlets that aren't manually cleaned up with ```.Dispose()``` can be reclaimed by using ```Disconnect-CMObject``` against an individual object.

#### Example
```powershell
# Reclaim all tracked objects
$o | Disconnect-CMObject```), or ```Disconnect-CMObject -All
```

Once an object is reclaimed, it can no longer be reused or passed to another cmdlet through the object pipeline.

```Stop-CMObjectTracking``` can be used to turn off object tracking. Previously allocated objects will remain active.

Unclaimed resources can cause Quota Violation errors to be raised by the SMS Provider. These quota issues typically manifest from working with large sets of SMS Provider objects or in long running environments.

> [!NOTE]
> This is an experimental feature and may be subject to change or removal in a future release. This feature is opt-in and isn't enabled by default.


## Cmdlet changes
The following changes have been made to existing cmdlets for this release. Changes may be new functionality, bug fixes, or deprecations. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

<!-- Misc -->
### PowerShell ISE
#### Bugs that were fixed
Powershell_ise.exe process may crash on exit when Verbose logging is enabled globally and the ConfigurationManager module has been imported.

### Task Sequence cmdlets
#### Bugs that were fixed
- ```New-CMTSRule```
    - Cmdlet may fail if a ```SecureString``` variable type is used.
- ```New-CMTSStepApplyOperatingSystem``` and ```Set-CMTSStepApplyOperatingSystem```
    - Cannot specify a null value for **DestinationLogicalDrive**.
    - Lowercase value for **DestinationLogicalDrive** may cause a UI validation failure.
- ```New-CMTSStepApplyWindowsSetting``` and ```Set-CMTSStepApplyWindowsSetting```
    - **Password** parameter usage may cause an error in the SMS Provider.
- ```New-CMTSStepInstallSoftware``` and ```Set-CMTSStepInstallSoftware```
    - Cmdlet incorrectly allows combining **Program** and **EnableContinueOnInstallError** parameters.

#### Non-breaking changes
Improved parameter validation.

<!-- ADD -->
### Add-CMComplianceSettingRegistryKeyValue
#### Bugs that were fixed
**ExpressionValue** doesn't support all combinations of settings with **ExpressionOperator**.
**Remediate** behavior not consistent with administrator console.
#### Non-breaking changes
**RemediateDword** parameter added to support an integer value for remediation.

### Add-CMManagementPoint
#### Non-breaking changes
Improved parameter validation.

### Add-CMMsiDeploymentType
#### Bugs that were fixed
Cmdlet doesn't validate for correct usage of **UninstallContentLocation** and **UninstallOption** parameter combinations.

### Add-CMScriptDeploymentType
#### Bugs that were fixed
Cmdlet incorrectly requires use of **Script** parameter when using **AddDetectionClause**.

### Add-CMSoftwareUpdatePoint
#### Bugs that were fixed
Cmdlet may return an error when adding a software update point to a remote system.

<!-- ENABLE -->
### Enable-CMSiteFeature
#### Bugs that were fixed
If pre-release features aren't enabled for the hierarchy, the cmdlet will fail with an incorrectly formatted error message.

<!-- GET -->
### Get-CMApplication
#### Breaking changes
Hidden applications are now no longer included by default. **ShowHidden** parameter has been added to force displaying hidden applications in the result set.

### Get-CMSiteInstallStatus
#### Bugs that were fixed
Cmdlet may run an invalid query against the SMS Provider.

### Get-CMSiteStatusMessage
#### Bugs that were fixed
Status message query may return duplicate messages.

<!-- NEW -->
### New-CMBootableMedia
#### Bugs that were fixed
**DistributionPoint** parameter doesn't ignore cloud-enabled distribution points.

### New-CMComplianceRuleFileFolderSize
#### Non-breaking changes
Improved parameter validation.

### New-CMDetectionClauseMacPackage
#### Bugs that were fixed
Improved parameter validation.

### New-CMDetectionClauseWindowsInstaller
#### Bugs that were fixed
**ProductCode** value isn't properly applied to the Setting object.

### New-CMExchangeServer
#### Non-breaking changes
**FullSyncSchedule** or **DeltaSyncMins** parameters are no longer mandatory and will apply a default schedule if not used.

### New-CMInventoryReportClass**
#### Non-breaking changes
**Name** parameter added for defining the class name.

### New-CMPrestagedMedia
#### Bugs that were fixed
Cmdlet fails when specifying an output file with a .wim extension.

### New-CMProgram
#### Bugs that were filed
**ProgramRunType** parameter value may be incorrectly applied to Program.

### New-CMSchedule
#### Bugs that were fixed
**RecurCount** shouldn't allow a value of ```0```.

### New-CMStandaloneMedia
#### Bugs that were fixed
Cmdlet may fail to create media if **MediaType** is ```Usb```.

#### Non-breaking changes
Improved parameter validation.

### New-CMStatusFilterRule
#### Non-breaking changes
Improved parameter validation.

### New-CMStorageFolder
#### Non-breaking changes
Improved parameter validation.

### New-CMTaskSequenceDeployment
#### Bugs that were fixed
Cmdlet may add two schedules when **ScheduleEvent** is used.

### New-CMWirelessProfile
#### Non-breaking changes
Improved parameter validation.

<!-- PUBLISH -->
### Publish-CMPrestageContent
#### Bugs that were fixed
**Application**/**ApplicationName**/**ApplicationId** parameter usage may cause the cmdlet to fail.

#### Non-breaking changes
Performance improvements.

<!-- SET -->
### Set-CMAntimalwarePolicy
#### Bugs that were fixed
**AddExcludedFilePath** doesn't create default exclusion rules.

### Set-CMApplication
#### Bugs that were fixed
Modifying an application with multiple display languages may cause unexpected changes to the application state.
#### Non-breaking changes
**AddAppCategory**, **AddUserCategory**, **RemoveAppCategory**, **RemoveUserCategory**, **CleanAppCategory**, and **CleanUserCategory** parameters have been added to support adding application categories by object.
#### Deprecations
**AppCategory** and **UserCategory** parameters have been superseded by the new [Add|Remove|Clean]AppCategory and [Add|Remove|Clean]UserCategory parameters.

### Set-CMBoundary
#### Bugs that were fixed
**NewName** parameter is missing.
#### Non-breaking changes
Improved parameter validation.

### Set-CMClientSettingClientcache
#### Deprecations
**EnableHttps** parameter is no longer supported.

### Set-CMManagementPoint
#### Non-breaking changes
Improved parameter validation.

### Set-CMMsiDeploymentType
#### Bugs that were fixed
Cmdlet doesn't validate for correct usage of **UninstallContentLocation** and **UninstallOption** parameter combinations.

### Set-CMPackage
#### Bugs that were fixed
**UseMeteredNetwork** parameter is missing.

### Set-CMSoftwareInventory
#### Non-breaking changes
**CleanTag1**, **CleanTag2**, **CleanTag3** parameters added to support removing tags.

**ParentSoftwareId**, **CategoryId** parameters added.

Improved parameter validation.

### Set-CMStatusFilterRule
#### Non-breaking changes
Improved parameter validation.

### Set-CMUserDataAndProfileConfigurationItem
#### Non-breaking changes
Improved parameter validation.


### Set-CMWirelessProfile
#### Non-breaking changes
Improved parameter validation around various profile creation scenarios.
