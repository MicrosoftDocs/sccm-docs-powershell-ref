---
title: Version 1710 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 1710.
ms.date: 11/20/2017
ms.topic: conceptual
ms.author: banreetkaur
author: Banreet
manager: apoorvseth
ROBOTS: NOINDEX
---

# Configuration Manager Cmdlet Library changes for Current Branch 1710

 >[!NOTE]
 > System Center Configuration Current Branch 1706 is the baseline for these changes. See [Configuration Manager Cmdlet Library changes for Current Branch 1706](1706_release_notes.md) for more details.

## Important changes

### Documentation library updates

For the latest cmdlet library documentation, see [ConfigurationManager module reference](/powershell/module/configurationmanager/).

### Removed cmdlets
The following cmdlets are no longer supported and have been removed:
- Invoke-CMAmtProvisioningDiscovery
- New-CMAmtProvisioningAccount
- Set-CMPowerControl

### Deprecated cmdlets
- ```Invoke-CMEndpointProtectionScan``` and ```Save-CMEndpointProtectionDefinition``` have been superseded by ```Invoke-CMClientAction```.

### Disable PSDrive auto-creation
When the ConfigurationManager.psd1 module is loaded, PowerShell automatically attempts to create a connection to the last SMS Provider that was accessed using the Configuration Manager console. In some scenarios, this behavior may not be desirable. A per-user registry key has been added that can disable this behavior and require manual drive creation. To configure this, use the registry key: ```HKEY_CURRENT_USER\Software\Microsoft\ConfigMgr10\PowerShell``` and set the value ```DisableCMDriveAutoCreate``` to a DWORD of 1 (drive auto-creation is disabled) or 0 (default behavior). Deleting ```DisableCMDriveAutoCreate``` also enables default behavior.

> [!NOTE]
> When drive auto-creation is disabled, the Configuration Manager console may report an error when launching a PowerShell window.

## Known issues
These are known issues with the Cmdlet Library that are not resolved in this release.

### Get-CMAadConditionalAccessPolicy and Set-CMAadConditionalAccessPolicy
64-bit PowerShell environment is required for these cmdlets.

#### Workaround
- None

### Import-CMSecurityRole
Cmdlet may fail with a DirectoryNotFoundException error locating the file ```SecuredRoles.xsd```.

#### Workaround
Ensure that ```Import-Module``` is called against the ```ConfigurationManager.psd1``` file, and not the logical path or module name.

### Get-CMSiteUpdateInstallStatus
Cmdlet may fail with a WqlQueryException error.

#### Workaround
- Use Invoke-CMWmiQuery to directly query the SMS_CM_UpdatePackTopLevelMonitoring class.

##### Example
```powershell
# Note: The PackageGuid value can be determined by running Get-CMSiteUpdateInstallStatus -Verbose and viewing the query details.
Invoke-CMWmiQuery "SELECT * FROM SMS_UpdatePackTopLevelMonitoring WHERE PackageGuid='...' ORDER BY StageId ASC"
```

### Set-CMSoftwareUpdatePoint
Changes to **Schedule** may not be reflected in the Configuration Manager console even though the underlying SMS Provider object has been changed.

#### Workaround
Quit and relaunch the Configuration Manager console.

## New cmdlets
These are newly-added cmdlets for this release that add new functionality or enhance the functionality of existing cmdlets.

### Device association cmdlets
```Get-CMResultantCollection``` will get the collections associated with a device.
```Get-CMResultantDeployment``` will get the deployments targeted to a device.

### Client inventory class management
New cmdlets have been added to support modifying inventory classes used for client inventory.
- Get-CMInventoryClass
- New-CMInventoryReportClass

### Task sequences
New cmdlets have been added to support modifying task sequence steps.
- Task sequence commands (Get, New, Remove, and Set verbs supported)
    - CMTaskSequenceStepApplyOperatingSystem
    - CMTaskSequenceStepApplyWindowsSetting

### Resource tracking and recovery (BETA)
New cmdlets have been added to support tracking SMS Provider objects used by the PowerShell runtime, and to clean up these resources when they are no longer needed.

- Disconnect-CMTrackedObject
- Start-CMObjectTracking
- Stop-CMObjectTracking

When ```Start-CMObjectTracking``` is run, the PowerShell runtime will track ```IResultObject``` objects created by Cmdlet Library cmdlets. Cmdlets that are not manually cleaned up with ```.Dispose()``` can be reclaimed by using ```Disconnect-CMTrackedObject``` against an individual object.

#### Example
```powershell
# Reclaim all tracked objects
$o | Disconnect-CMTrackedObject```), or ```Disconnect-CMTrackedObject -All
```

Note that once an object is reclaimed, it can no longer be reused or passed to another cmdlet through the object pipeline.

```Stop-CMObjectTracking``` can be used to turn off object tracking. Note that previously allocated objects will remain active.

Unclaimed resources can cause Quota Violation errors to be raised by the SMS Provider. These issues typically manifest from working with very large sets of SMS Provider objects or in very long running environments

> [!NOTE]
> This is an experimental feature and may be subject to change or removal in a future release. This feature is opt-in and is not enabled by default.


## Cmdlet changes
The following changes have been made to existing cmdlets for this release. Changes may be new functionality, bug fixes, or deprecations, and may be breaking. If you use one of the cmdlets or feature areas listed in this section, please carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

### Compliance setting and rule cmdlets
#### Bugs that were fixed
**RuleDescription** value may not apply to the Rule. (Cmdlets that support rule creation or modification)

Cannot set value for "default" registry key (Add/Set-CMComplianceSettingRegistryKeyValue, New-CMDetectionClauseRegistryKeyValue).

NullReferenceException may be raised (New-CMComplianceRuleAssembly)

Missing DataType support (Add-CMComplientSettingREgistryKeyValue)

### Add-CMApplicationCatalogWebsitePoint
#### Bugs that were fixed
Improved error handling and reporting.

### Add/Set-CMDataWarehouseServicePoint
#### Non-breaking changes
**DataWarehouseSqlPort** supports port value from 1-65535.
**DaysOfWeek** parameter now supports value of ```Daily```.

### Add/Set-CMExchangeServer
#### Bugs that were fixed
**EmailAddress** parameter value may not apply to the Exchange server configuration.

### Add-CMMsiDeploymentType
#### Bugs that were fixed
**ContentLocation** parameter is required when using script detection.
Added new **UninstallContentLocation** and **UninstallOption** parameters.

#### Non-breaking changes
Improved validation for **ProductCode** parameter.

### Add-CMScriptDeploymentType
#### Non-breaking changes
Improved validation for **ProductCode** parameter.
Added new **UninstallContentLocation** and **UninstallOption** parameters.

### Get-CMDeploymentTypeDependencyGroup
#### Non-breaking changes
Cmdlet now supports pipelined value from ```Get-CMDeploymentType```.

### Get-CMSiteStatusMessage
#### Bugs that were fixed
Not all messages are returned when filtering with the **Severity** parameter.

### Invoke-CMClientAction (formerly Invoke-CMClientNotification)
#### Non-breaking changes
**ActionType** parameter that accepts all client notification types.
> [!NOTE]
> ```RequestScriptExecution``` is not supported at this time.

#### Deprecations
**NotificationType** has been superseded by **ActionType**

### New-CM*Deployment
#### Bugs that were fixed
Cmdlet allows combining **CollectionId**, **CollectionName**, and **Collection** parameters which can lead to undefined behavior.

### New-CMBootableMedia
#### Bugs that were fixed
Unable to create media as SiteBased.

### New-CMWirelessProfile
#### Bugs that were fixed
Cmdlet fails to run in a 64-bit PowerShell environment.

Cmdlet may return an error if specifying a value for the **ClientCertificate** parameter.

### Remove-CMCorpOwnedDevice
#### Bugs that were fixed
Cannot remove device when using pipelined object.

Device name is not reported when using **WhatIf** or **Confirm**.

### Remove-CMStateMigrationPoint
#### Breaking changes
Additional confirmation will be required if there is user data stored on the state migration point. Note: **Force** will bypass this confirmation.

### Save-CMSoftwareUpdate
#### Non-breaking changes
Added **RetryCount** and **RetryDelaySec** parameters to reattempt downloads after a failure.

### Set-CMAccessAccount
#### Bugs that were fixed
**PassThru** may not return an updated object.

### Set-CMAntimalwarePolicy
#### Bugs that were fixed
Cannot use wildcard characters with **AddExcludedFilePath** parameter.

Unable to configure ```FallbackOrder``` for a given policy

#### Non-breaking changes
Added new parameters for managing threat lists: **AddThreat**, **RemoveThreat**, and **CleanThreat**. AddThreat accepts a hashtable with the key being the name, and the value being of type ```Microsoft.ConfigurationManagement.Cmdlets.EP.Commands.DefaultActionMediumAndLowType```.

#### Deprecations
**ThreatName** and **OverrideAction** parameters have been superseded by **AddThreat**, **RemoveThreat**, and **CleanThreat**.

### Set-CMClientSettingComputerAgent
#### Deprecations
**HealthAttestationUrl** parameter as it is no longer utilized by the product.

### Set-CMClientSettingHardwareInventory
#### Non-breaking changes
**AddInventoryReportClass**, **CleanInventoryReportClass**, and **RemoveInventoryReportClass** parameters support modifying the hardware inventory collected by clients.

### Set-CMMsiDeploymentType
#### Non-breaking changes
Improved validation for **ProductCode** parameter.

### Set-CMScriptDeployment
#### Bugs that were fixed
Application object in SMS Provider may not automatically unlock if the cmdlet fails preventing further modifications until the lock expires.

### Set-CMScriptDeploymentType
#### Non-breaking changes
Improved validation for **ProductCode** parameter.

### Set-CMSoftwareUpdatePointComponent
#### Non-breaking changes
Added new **ContentFileOption** parameter for configuring update download behavior.

### Set-CMSiteMaintenanceTask
#### Non-breaking changes
Improved error reporting

### Set-CMWirelessProfile
#### Bugs that were fixed
Cmdlet fails to run in a 64-bit PowerShell environment.

MismatchedPSTypeName error may be raised when using the object pipeline.

**ProxyAddress** and **ProxyPort** does not validate using the same rules as the Configuration Manager console.

Specifying **ProxyAddress** without **ProxyPort** may cause an invalid configuration to be created.

**SecurityAuthentication** can be changed with configurations that do not support this.

**EapType** must be combined with **SecurityAuthentication** even when the latter is not changing.

#### Non-breaking changes
Added **RootCertificate**, **ClientCertificate**, and **RememberCredentials** parameters.

Improved functionality for configuring a MSCHAPv2 wireless policy.

### Sync-CMSoftwareUpdate
#### Non-breaking changes
Cmdlet no longer requires any parameters to be specified.
> [!NOTE]
> When no parameters are defined, ```-ForceSync $true``` is implied.
