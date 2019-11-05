---
title: Version 1806 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 1806. 
ms.date: 09/19/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Configuration Manager Cmdlet Library changes for version 1806

*Applies to: System Center Configuration Manager (Current Branch)*

 > [!NOTE]  
 > Configuration Manager version 1802 is the baseline for these changes. For more information, see [Configuration Manager Cmdlet Library changes for version 1802](https://docs.microsoft.com/powershell/sccm/1802_release_notes).


## Important changes

### Removed cmdlets
- ```Add-CMWindowsMobileDeploymentType```
- ```Set-CMWindowsMobileDeploymentType```

### Deprecated cmdlets
- ```New-CMGlobalCondition``` and ```Set-CMGlobalCondition``` have been superseded by the new family of global condition cmdlets.



## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To leave bug reports, use the [Feedback Hub](https://docs.microsoft.com/sccm/core/understand/find-help). For feature requests, use [UserVoice](https://configurationmanager.uservoice.com).



## Known issues
The following items are known issues with the Cmdlet Library that aren't resolved in this release.

### Get-CMDevice
Cmdlet may not return expected properties for a device.

>[!NOTE]
> This issue is currently scheduled to be addressed in a future update rollup.

#### Workaround
- Specify **CollectionName**, **CollectionId**, or **Collection** parameter value.

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

### Compliance settings cmdlet improvements
#### Bugs that were fixed
- Add-CMComplianceSettingRegistryKeyValue may not honor **DataType** parameter value.
- Certain values for **ExpressionOperator** may cause the console to unexpectedly quit when the setting is viewed.
- ConvertFrom-CMConfigurationItem may fail with a NullReferenceException.
#### Non-breaking changes
- New/Set-CMGlobalConditionActiveDirectoryQuery improved error messages when validation failures occur.
- Improved validation to better align with console.

### Task sequence cmdlet improvements
#### Breaking changes
- New-CMTSStepPrestartCheck **CheckSpace** value will be set to true in the created task sequence step if it not specified.
- Get-CMTSStep* no longer accept **WhatIf** and **Confirm** parameters.
#### Bugs that were fixed
- New-CMTSStep* cmdlets may ignore **WhatIf** and **Confirm** parameters if specified.
#### Non-breaking changes
- New/Set-CMTSStepSetVariable new **IsMasked** parameter to hide variable values.
- Improved validation to better align with console.

### Export cmdlets improvements
- Changes affect Export-CMPackage, Export-CMAntimalwarePolicy, Export-CMDriverPackage, Export-CMTaskSequence, Export-CMDeviceCollection, and Export-CMUserCollection.
#### Bugs that were fixed
- Improved file path validation.
- Improved handling of I/O errors.
- Export-CMDriverPackage may create an empty driver package.
#### Non-breaking changes
- New **Force** parameter can be used to force overwriting an existing file.

### Add-CMApplication
#### Bugs that were fixed
- Publisher and Software Version as configured by this cmdlet may not show in Software Center.
#### Non-breaking changes
- **Keyword** parameter now supports array of strings.
- **AppCatalog** parameter now supports an array of application catalogs.

### Add-CMDataWarehouseServicePoint
#### Non-breaking changes
- New **DataRetentionDays** parameter allows for configuring data retention policy.

### Add-CMDeviceCollectionDirectMembershipRule
#### Bugs that were fixed
- Adding new rules may delete existing rules.

### Add-CMDeviceAffinityToUser
#### Non-breaking changes
- **DeviceId** and **DeviceName** parameters now support arrays of values.

### Add-CMDistributionPoint
#### Non-breaking changes
- New **EnableNonWdsPxe** parameter allows for WDS-less PXE configuration.
- Improved validation for **\*ContentLibraryLocation** and **\*ContentShare** parameters.

### Add-CMDriverToDriverPackage
#### Non-breaking changes
- New <em>**UpdateDistributionPoint</em>* parameter allows suppressing distribution point updates.

### Add-CMReportingServicePoint
#### Bugs that were fixed
- Reporting service point that isn't co-located on the site server isn't properly configured.

### Add-CMUserAffinityToDevice
#### Non-breaking changes
- **UserId** and **UserName** parameters now support arrays of values.

### Get-CMSiteUpdateInstallStatus
#### Bugs that were fixed
- ```PostInstallation``` value for **Step** parameter is not recognized by cmdlet.

### New-CMApplicationDeployment
#### Non-breaking changes
- Improvements to parameter validation.

### New-CMBootableMedia
#### Bugs that were fixed
- Invalid folder path may be specified for media creation.

### New-CMCloudDistributionPoint
#### Bugs that were fixed
- Cmdlet fails to create cloud distribution point.

### New-CMCloudManagementGateway
#### Bugs that were fixed
- Cloud management gateway may be unable to communicate with Azure due to incorrect configuration settings.

### New-CMExchangeServer
#### Non-breaking changes
- Improvements to parameter validation.

### New-CMTaskSequenceDeployment
#### Bugs that were fixed
- **CollectionName** parameter allows for user collections to be specified.
- Improper locking of SMS_TaskSequence object.

### Remove-CMDeviceAffinityToUser
#### Non-breaking changes
- **DeviceId** and **DeviceName** parameters now support arrays of values.

### Remove-CMDeviceCollectionDirectMembershipRule
#### Non-breaking changes
- Performance improvements when modifying collections with large number of rules.

### Remove-CMDriverFromDriverPackage
#### Non-breaking changes
- New <em>**UpdateDistributionPoint</em>* parameter allows suppressing distribution point updates.

### Remove-CMUserAffinityToDevice
#### Non-breaking changes
- **UserId** and **UserName** parameters now support arrays of values.

### Save-CMSoftwareUpdate
#### Bugs that were fixed
- Warning message if update download fails may show incorrect count.

### Set-CMApplication
#### Bugs that were fixed
- Publisher and Software Version as configured by this cmdlet may not show in Software Center.
#### Non-breaking changes
- **Keyword** parameter now supports array of strings.
- New **AddAppCatalog**, **RemoveAppCatalog**, and **ClearAppCatalog** parameters for modifying the application catalogs associated with the application.

### Set-CMApplicationDeployment
#### Non-breaking changes
- Improvements to parameter validation.

### Set-CMDataWarehouseServicePoint
#### Non-breaking changes
- New **DataRetentionDays** parameter allows for configuring data retention policy.

### Set-CMDistributionPoint
#### Bugs that were fixed
- Cmdlet may fail if updating a distribution point with a certificate that already exists.
#### Non-breaking changes
- New **EnableNonWdsPxe** parameter allows for WDS-less PXE configuration.
- Improved validation for **\*ContentLibraryLocation** and **\*ContentShare** parameters.

### Set-CMExchangeServer
#### Non-breaking changes
- Improvements to parameter validation.

### Set-CMIntuneSubscriptionWindowsProperty
#### Bugs that were fixed
- **CertificatePath** value may not appear in the console.

### Set-CMSite
#### Non-breaking changes
- Performance improvements.

### Set-CMSoftwareUpdatePointComponent
#### Bugs that were fixed
- Pipelined object from Get-CMSiteComponent isn't recognized.

### Start-CMApplicationDeployment
#### Non-breaking changes
- New **UpdateSupersedence** parameter has been added.

### Start-CMDistributionPointUpgrade
#### Non-breaking changes
- New **EnableNonWdsPxe** parameter allows for WDS-less PXE configuration.
