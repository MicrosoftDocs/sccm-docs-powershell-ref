---
title: Version 1910 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 1910. 
ms.date: 11/25/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Configuration Manager Cmdlet Library changes for version 1910

*Applies to: Configuration Manager (current branch)*

> [!NOTE]  
> Configuration Manager current branch version 1906 is the baseline for these changes. For more information, see [Configuration Manager Cmdlet Library changes for version 1906](https://docs.microsoft.com/powershell/sccm/1906-release-notes).

## Important changes

### New cmdlets

#### New-CMDuplicateHardwareIdGuid

Use this cmdlet to add duplicate hardware identifiers by GUID.

``` PowerShell
New-CMDuplicateHardwareIdGuid -Id 24D0F753-B2E2-4D9C-B07C-099C4FC1EF3C
```

#### New-CMDuplicateHardwareIdMacAddress

Use this cmdlet to add duplicate hardware identifiers by MAC address.

``` PowerShell
New-CMDuplicateHardwareIdMacAddress -MacAddress 01:02:03:04:05:E0
```

#### New-CMThirdPartyUpdateCatalog

Use this cmdlet to create a new third-party updates catalog.

``` PowerShell
New-CMThirdPartyUpdateCatalog -DownloadUrl $downloadUrl -PublisherName $publisher -Name $name -Description $description -SupportUrl $supportUrl -SupportContact $supportContact
```

#### Get-CMThirdPartyUpdateCatalog

Use this cmdlet to get a third-party updates catalog.

```PowerShell
Get-CMThirdPartyUpdateCatalog
Get-CMThirdPartyUpdateCatalog -Id $id
Get-CMThirdPartyUpdateCatalog -Name $name
Get-CMThirdPartyUpdateCatalog -SiteCode $siteCode
Get-CMThirdPartyUpdateCatalog -IsSyncEnabled $true
Get-CMThirdPartyUpdateCatalog -IsCustomCatalog $true
```

#### Set-CMThirdPartyUpdateCatalog

Use this cmdlet to modify a third-party updates catalog.

``` PowerShell
Set-CMThirdPartyUpdateCatalog -Name $name -NewName $newName
Set-CMThirdPartyUpdateCatalog -ThirdPartyUpdateCatalog $catalog -Description $newdescription
$catalog | Set-CMThirdPartyUpdateCatalog -SupportContact $newSupportContact -SupportUrl $newSupportUrl
```

#### Remove-CMDuplicateHardwareIdGuid

Use this cmdlet to remove duplicate hardware identifiers by GUID.

``` PowerShell
Remove-CMDuplicateHardwareIdGuid -Id 24D0F753-B2E2-4D9C-B07C-099C4FC1EF3C
Remove-CMDuplicateHardwareIdGuid -InputObject $myGuid #(<IResultObject#SMS_CommonSmbiosGuids>)
```

#### Remove-CMDuplicateHardwareIdMacAddress

Use this cmdlet to remove duplicate hardware identifiers by MAC address.

``` PowerShell
Remove-CMDuplicateHardwareIdMacAddress -MacAddress 01:02:03:04:05:E0
Remove-CMDuplicateHardwareIdMacAddress -InputObject $myMacAddress #(<IResultObject#SMS_CommonMacAddresses>)
```

#### Remove-CMThirdPartyUpdateCatalog

Use this cmdlet to remove a third-party updates catalog.

``` PowerShell 
Remove-CMThirdPartyUpdateCatalog -Id $catalog.ID -Force
Remove-CMThirdPartyUpdateCatalog -Name $catalog.Name -Force
Remove-CMThirdPartyUpdateCatalog -ThirdPartyUpdateCatalog $catalog -Force
$catalog | Remove-CMThirdPartyUpdateCatalog -Force
```


### Removed cmdlets

The following cmdlets have been removed with the end of hybrid service:

- Add-CMIntuneSubscription
- Add-CMMdmEnrollmentManager (Add-CMIntuneDeviceEnrollmentManager)
- Export-CMWindowsEnrollmentProfile
- Get-CMConditionalAccessPolicy (Get-CMOnPremConditionalAccessPolicy)
- Get-CMCorpOwnedDevice
- Get-CMDeviceActionState (Get-CMDeviceAction)
- Get-CMIntuneSubscription
- Get-CMIosEnrollmentProfile
- Get-CMMdmEnrollmentManager (Get-CMIntuneDeviceEnrollmentManager)
- Get-CMWindowsEnrollmentProfile
- Get-CMWindowsEnrollmentProfilePackage
- Invoke-CMDeviceAction
- New-CMApnsCertificateRequest
- New-CMConditionalAccessPolicy (New-CMOnPremConditionalAccessPolicy)
- New-CMDepTokenRequest
- New-CMIosEnrollmentProfile
- New-CMWindowsEnrollmentProfile
- Remove-CMConditionalAccessPolicy (Remove-CMOnPremConditionalAccessPolicy)
- Remove-CMCorpOwnedDevice
- Remove-CMIntuneSubscription
- Remove-CMIosEnrollmentProfile
- Remove-CMMdmEnrollmentManager (Remove-CMIntuneDeviceEnrollmentManager)
- Remove-CMWindowsEnrollmentProfile
- Remove-CMWindowsEnrollmentProfilePackage
- Set-CMConditionalAccessPolicy (Set-CMOnPremConditionalAccessPolicy)
- Set-CMIntuneSubscription
- Set-CMIntuneSubscriptionAndroidProperty (Set-CMIntuneSubscriptionAndroidProperties)
- Set-CMIntuneSubscriptionAppleDepProperty
- Set-CMIntuneSubscriptionAppleProperty

  (aliases:)
  - Set-CMIntuneSubscriptionMacOSProperties
  - Set-CMIntuneSubscriptionIosProperties
  - Set-CMIntuneSubscriptionMacOSProperty
  - Set-CMIntuneSubscriptionIosProperty
  - Set-CMIntuneSubscriptionAppleMdmProperty

- Set-CMIntuneSubscriptionPassportForWorkProperty
- Set-CMIntuneSubscriptionWindowsPhoneProperty (Set-CMIntuneSubscriptionWindowsPhoneProperties)
- Set-CMIntuneSubscriptionWindowsProperty (Set-CMIntuneSubscriptionWindowsProperties)
- Set-CMIosEnrollmentProfile
- Set-CMIosEnrollmentProfileAssignment
- Set-CMWindowsEnrollmentProfile

### Deprecated cmdlets

None

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

### Add-CMDistributionPoint

#### Non-breaking changes

Now the cmdlet supports use of a duplicated certificate by the `-Force` switch:

### Add-CMMsiDeploymentType

#### Bugs that were fixed

Fixed a validation issue for uninstall content location.

### Import-CMDriver

#### Bugs that were fixed

- Fixed an issue for driver that uses txtsetup.oem.
- Fixed an issue if the target driver package has never been distributed before.

### New-CMApplicationDeployment

#### Bugs that were fixed

Fixed bad disposal issue.

### New-CMDriverPackage

#### Non-breaking changes

Added new parameters for manufacturer and model. You can use them for managing the driver catalog, and with task sequence pre-caching.

- `-DriverManufacturer [string]`
- `-DriverModel [string]`

##### Example

```PowerShell
Get-CMDriverPackage | Set-CMDriverPackage -DriverManufacturer "Microsoft" -DriverModel "Surface 2"
Set-CMDriverPackage -PackageId MCS00091 -DriverManufacturer "Microsoft" -DriverModel "Surface 2"
Get-CMDriverPackage | Where-Object {$_.Name -like "Surface Book 2"} | Set-CMDriverPackage -DriverManufacturer "Microsoft" -DriverModel "Surface 2"
New-CMDriverPackage -Name "Surface Book 2 Drivers" -Description "Some descriptive text" -DriverManufacturer "Microsoft" -DriverModel "Surface 2"
```

### New-CMSoftwareUpdateAutoDeploymentRule

#### Non-breaking changes

The cmdlet now supports the **No Deployment Package** option when creating the rule.

##### Example

```PowerShell
New-CMSoftwareUpdateAutoDeploymentRule -Collection $collection -Name $name -Architecture X86, Itanium, X64
```

### New-CMTaskSequence

#### Non-breaking changes

This cmdlet has a new parameter to support high-performance option in task sequence:

`-HighPerformance [bool]`

### New-CMTSStepApplyWindowsSetting

#### Non-breaking changes

This cmdlets includes new parameters to support the new locale settings in the task sequence step:

- `-InputLocale [string]`
- `-SystemLocale [string]`
- `-UserLocale [string]`
- `-UILanguage [string]`
- `-UILanguageFallback [string]`

##### Example

To set input locale to Russian (Russia), specify string `ru-ru`: `-InputLocale "ru-ru"`

### New-CMTSStepDownloadPackageContent

#### Bugs that were fixed

Fixed a duplicated package checking issue for adding package.

### New-CMTSStepRunCommandLine

#### Non-breaking changes

Added a new parameter to support output variable option: `-OutputVariableName [string]`

### Get-CMDevice

#### Bugs that were fixed

Fixed a device query issue in collection that's without access permission.

### Get-CMScript

#### Bugs that were fixed

Fixed a wildcard support issue.

### Remove-CMApplicationDeployment

#### Bugs that were fixed

Fixed bad disposal issue.

### Remove-CMDevice

#### Bugs that were fixed

Fixed a device query issue.

### Set-CMBootImage

#### Non-breaking changes

Added a new parameter to support keyboard layout setting: `-InputLocale [string]`

### Set-CMClientSettingClientPolicy

#### Non-breaking changes

Added a new parameter to support user policy on task sequence option: `-EnableUserPolicyOnTS [bool]`

### Set-CMClientSettingSoftwareUpdate

#### Non-breaking changes

Added new a parameter to support third-party updates: `-EnableThirdPartyUpdates [bool]`

##### Example

``` PowerShell
Set-CMClientSettingSoftwareUpdate -Name $clientDeviceSettingName -Enable $true -EnableThirdPartyUpdates $true
Set-CMClientSettingSoftwareUpdate -DefaultSetting -Enable $true -EnableThirdPartyUpdates $true
```

### Set-CMDistributionPoint

#### Bugs that were fixed

- Fixed a reassign site code issue.
- Fixed a device query issue.

#### Non-breaking changes

The cmdlet now supports use of a duplicated certificate by the `-Force` switch:

### Set-CMDriverPackage

#### Non-breaking changes

Added new parameters to support manufacturer and model settings:

- `-DriverManufacturer [string]`
- `-DriverModel [string]`

### Set-CMMsiDeploymentType

#### Bugs that were fixed

Fixed a validation issue for uninstall content location.

### Set-CMScript

#### Bugs that were fixed

- Fixed a script text value issue.
- Fixed a wildcard support issue.

### Set-CMSite

#### Bugs that were fixed

- Fixed a script text value issue.
- Fixed a wildcard support issue.

### Set-CMSiteSystemServer

#### Non-breaking changes

Fixed a proxy-related properties setting issue.

### Set-CMSoftwareUpdateAutoDeploymentRule

#### Non-breaking changes

Added new parameters to allow user to set the deployment package for the existing software update auto deployment rule.

- `-DeploymentPackageName [string]`
- `-DeploymentPackage [IResultObject]`

##### Example

``` PowerShell
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -DeploymentPackageName $null
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -DeploymentPackageName $packageName
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -DeploymentPackage $null
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -DeploymentPackage $package
```

### Set-CMSoftwareUpdateDeployment

#### Bugs that were fixed

Fixed properties setting issue for `-DisableOperationsManagerAlert` and `-GenerateOperationsManagerAlert`.

### Set-CMSoftwareUpdateDeploymentPackage

#### Non-breaking changes

Added Force switch to allow you to force remove an expired NAP update: `-Force [switch]`

### Set-CMSoftwareUpdatePointComponent

#### Non-breaking changes

- Added new parameters to support third-party updates options:
  - `-EnableThirdPartyUpdates [bool]`
  - `-EnableManualCertManagement [bool]`

- Added new parameters to support feature update run time options:
  - `-NonFeatureUpdateMaxRuntimeMins [int]`
  - `-FeatureUpdateMaxRuntimeMins [int]`

##### Example

``` PowerShell
Set-CMSoftwareUpdatePointComponent -SiteCode $Site.SiteCode -EnableThirdPartyUpdates $true
Set-CMSoftwareUpdatePointComponent -SiteCode $Site.SiteCode -EnableManualCertManagement $true
```

### Set-CMTaskSequence

#### Non-breaking changes

Added a new parameter to support the high-performance option in the task sequence: `-HighPerformance [bool]`

### Set-CMTSStepApplyWindowsSetting

#### Non-breaking changes

Added new parameters to support locale settings in this task sequence step:

- `-InputLocale [string]`
- `-SystemLocale [string]`
- `-UserLocale [string]`
- `-UILanguage [string]`
- `-UILanguageFallback [string]`

##### Example

To set input locale to Russian (Russia), specify string `ru-ru`: `-InputLocale "ru-ru"`

### Set-CMTSStepDownloadPackageContent

#### Bugs that were fixed

- Fixed a duplicated package checking issue for adding package.
- Fixed a validation issue for adding/removing package

### Set-CMTSStepRunCommandLine

#### Non-breaking changes

New parameter to support output variable option: `-OutputVariableName [string]`

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To submit bug reports, use [send a smile in the Configuration Manager console](https://docs.microsoft.com/sccm/core/understand/find-help#product-feedback). For new feature requests, use [UserVoice](https://configurationmanager.uservoice.com).
