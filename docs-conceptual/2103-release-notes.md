---
title: Version 2103 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2103.
ms.date: 03/26/2021
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.localizationpriority: low
ms.author: banreetkaur
author: Banreet
manager: apoorvseth
---

# Configuration Manager cmdlet library changes for version 2103

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2103.

> [!NOTE]
> Configuration Manager current branch version 2010 is the baseline for these changes. For more information, see [Configuration Manager cmdlet library changes for version 2010](2010-release-notes.md).

## Known issue with updateable PowerShell help

<!-- 8617455 -->

Starting in version 2010, you could use the **Update-Help** cmdlet to download the latest information for the Configuration Manager PowerShell module.

In version 2103, the PowerShell module structure changed from 29 DLLs to two. The PowerShell XML help files are associated with the DLL for the cmdlets. So the version 2010 help content is incompatible with a version 2103 console, and the version 2103 help content is incompatible with a version 2010 console.

Because of this change in how the updateable content is structured and published with the release of version 2103, don't use **Update-Help** on a version 2010 site. Update the site to version 2103, and then update the local help content.

The cmdlet will successfully download content on a version 2010 console, but **Get-Help** will only return default usage information. This behavior is because PowerShell isn't able to find the cmdlet information in the right XML file, which is different now. Before the release of version 2103, if you used **Update-Help** with a version 2010 site, you can continue to use **Get-Help** now.

Similarly, if you used **Update-Help** on a version 2010 site, after you update to version 2103, run **Update-Help** again to get the compatible version of the help content. Otherwise **Get-Help** will only return default usage information.

> [!NOTE]
> This issue is unique to version 2010. Because of how the structure changed, it shouldn't be an issue for later versions.

## PowerShell module

If the Configuration Manager console on the device hasn't already connected to a site, if you manually import the ConfigurationManager module, it creates a PowerShell drive for the site based on the default SMS Provider.

Starting in version 2103, the ConfigurationManager PowerShell module requires Microsoft .NET version 4.7.2 or later.

## Cmdlets that don't support PowerShell version 7

<!-- 6337796 -->
While Configuration Manager cmdlets provide general [support for PowerShell version 7](/powershell/sccm/overview#support-for-powershell-version-7), the following cmdlets don't support PowerShell 7:

- Import-CMPackage
- Import-CMDriverPackage
- Import-CMTaskSequence
- Export-CMPackage
- Export-CMDriverPackage
- Export-CMTaskSequence

They require the .NET Framework instead of .NET Core that's used with PowerShell version 7.

Starting in version 2103, if you try to use these cmdlets in a PowerShell version 7 session, they fail with the following error: `This cmdlet only supports the ".NET Framework" runtime.`

## New cmdlets

<!-- - [<cmdlet>](/powershell/module/configurationmanager/): -->

- [Get-CMApplicationGroup](/powershell/module/configurationmanager/get-cmapplicationgroup): Use this cmdlet to get an application group.
- [Get-CMDuplicateHardwareIdGuid](/powershell/module/configurationmanager/get-cmduplicatehardwareidguid): Get duplicate hardware identifiers by GUID.
- [Get-CMDuplicateHardwareIdMacAddress](/powershell/module/configurationmanager/get-cmduplicatehardwareidmacaddress): Get duplicate hardware identifiers by MAC address.
- [New-CMApplicationGroup](/powershell/module/configurationmanager/new-cmapplicationgroup): Use this cmdlet to create a new application group.
- [Publish-CMThirdPartySoftwareUpdateContent](/powershell/module/configurationmanager/publish-cmthirdpartysoftwareupdatecontent): Use this cmdlet to publish third-party update content.
- [Remove-CMApplicationGroup](/powershell/module/configurationmanager/remove-cmapplicationgroup): Use this cmdlet to remove a specific application group.
- [Remove-CMClientSettingDeployment](/powershell/module/configurationmanager/remove-cmclientsettingdeployment): Use this cmdlet to remove a specific deployment of a client setting.
- [Set-CMApplicationGroup](/powershell/module/configurationmanager/set-cmapplicationgroup): Use this cmdlet to configure a specific application group.
- [Set-CMCISupportedPlatform](/powershell/module/configurationmanager/set-cmcisupportedplatform): Use this cmdlet to configure the platforms for a configuration item.
- [Sync-CMCloudManagementGateway](/powershell/module/configurationmanager/sync-cmcloudmanagementgateway): Synchronize the configuration of a cloud management gateway (CMG) to Azure.

<!-- 
## Deprecated and removed cmdlets

The following cmdlet is deprecated:

- [Set-CMClientSetting](/powershell/module/configurationmanager/Set-CMClientSetting)
 -->

<!-- 
## Known issues

None
 -->

## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
For more information, see [](/powershell/module/configurationmanager/).
**Breaking changes**
**Bugs that were fixed**
**Non-breaking changes**
**Deprecations**
-->

### Fast support

The following cmdlets now support the **Fast** parameter. Use this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause more network traffic and affect cmdlet performance.

- Get-CMAlert
- Get-CMAlertSubscription
- Get-CMBaseline
- Get-CMBaselineDeployment
- Get-CMBaselineDeploymentStatus
- Get-CMClientCertificatePfx
- Get-CMComplianceRule
- Get-CMComplianceSetting
- Get-CMConfigurationPlatform
- Get-CMConfigurationPolicyDeployment
- Get-CMDriver
- Get-CMDriverPackage
- Get-CMTaskSequence
- Get-CMTaskSequenceDeployment

### Add-CMFallbackStatusPoint

**Non-breaking changes**

Fixed an inconsistent parameter name.

### Copy-CMCollection

**Non-breaking changes**

Fixed validation with **NewName** parameter to align with console.

### Get-CMDeploymentStatusDetails

**Non-breaking changes**

- Fixed input object type validation issue for types like **SMS_DCMDeploymentErrorStatus**, **SMS_DCMDeploymentNonCompliantStatus**, and **SMS_DCMDeploymentCompliantStatus**.
- Fixed output invalid class type issue by changing output object type **SMS_AppDeploymentRequirementsNotMetStatus** to **SMS_AppDeploymentRequirementsNotMetAssetDetails**.
- Changed the output object type from **SMS_AppDeploymentAssetDetails** to [SMS_AppDeploymentErrorAssetDetails](/mem/configmgr/develop/reference/apps/sms_appdeploymenterrorassetdetails-server-wmi-class) to get more error details.
- Added an input object type **SMS_UpdateDeploymentSummary** so that this cmdlet can get update deployment details. When passing the output of [Get-CMSoftwareUpdateDeploymentStatus](/powershell/module/configurationmanager/get-cmsoftwareupdatedeploymentstatus) to Get-CMDeploymentStatusDetails, it returns deployment details from **SMS_SUMDeploymentAssetDetails**.

### Get-CMDriver

**Non-breaking changes**

Add ability to filter by parameter **AdministrativeCategory**.

```powershell
$category1 = Get-CMCategory -CategoryType DriverCategories -Name 'OEM 1'
$category2 = Get-CMCategory -CategoryType DriverCategories -Name 'OEM 2'
$categories = $category1,$category2

Get-CMDriver -AdministrativeCategory $categories
```

### Get-CMPackage

**Non-breaking changes**

Added parameter **PackageType** for retrieving specific package type.

### Get-CMSoftwareUpdateDeployment

**Non-breaking changes**

Fixed an issue when deploying updates with no package.

### New-CMApplication

**Bugs that were fixed**

Fixed a Software Center display issue when installing apps created with the time format "yyyy/MM/dd".

### New-CMCertificateProfileScep

**Bugs that were fixed**

Fixed an issue for parameter **SanType**.

### New-CMCollection

**Non-breaking changes**

Fixed validation with **Name** parameter to align with console.

### New-CMOperatingSystemImage

**Non-breaking changes**

Added parameter **Index**. When you add this parameter, the site extracts a single index image from a multi-index image. It then places the new image in the same source folder as the original image.

### New-CMOperatingSystemInstaller

**Non-breaking changes**

Added parameter **Index**. When you add this parameter, the site replaces the current multi-index image with a new single index image.

### New-CMTSRule

**Non-breaking changes**

Parameter **ReferencedVariableOperator** has another possible value: `NotLike`.

### New-CMTSStepConditionVariable

**Non-breaking changes**

Parameter **OperatorType** has another possible value: `NotLike`

### New-CMSoftwareUpdateAutoDeploymentRule

**Breaking changes**

Fixed an issue for parameter **O365LanguageSelection**. You now need to specify a language with a country/region name. This change aligns this parameter with the options in the Configuration Manager console. For example, `-O365LanguageSelection "English (United States)"`

### Set-CMCertificateProfileScep

**Bugs that were fixed**

Fixed an issue for parameter **SanType**.

### Set-CMClientPushInstallation

**Non-breaking changes**

Add parameter **AllownNTLMFallback** to enable NTLM fallback.

### Set-CMCollection

**Non-breaking changes**

Fixed validation with **NewName** parameter to align with console.

### Set-CMEmailProfile

**Non-breaking changes**

- Fixed issue with **NewName** parameter when you specify `sAMAccountName` as the account user name.
- Fixed a parameter issue when resolving **DomainName**.

### Set-CMFallbackStatusPoint

**Non-breaking changes**

Fixed an inconsistent parameter name.

### Set-CMThirdPartyUpdateCatalog

**Non-breaking changes**

Add parameters **CategoryNamePublishOption** and **CategoryIdPublishOption**. Use these parameters to set the category publish option when you subscribe to a v3 catalog.

```powershell
$id = "5768207d-6c40-465b-ad65-50501661368f"
$option = [Microsoft.ConfigurationManagement.Cmdlets.Sum.Commands.PublishOptionType]::MetadataOnly
$idOptionPair = @{$id = $option}
Set-CMThirdPartyUpdateCatalog -CatalogName 'pmp' -CategoryIdPublishOption $idOptionPair -Subscribe -Force
```

```powershell
$name = "2BrightSparks"
$name1 = "8x8, Inc."
$option = [Microsoft.ConfigurationManagement.Cmdlets.Sum.Commands.PublishOptionType]::MetadataOnly
$nameOptionPair = @{$name = $option; $name1 = $option}
Set-CMThirdPartyUpdateCatalog -CatalogName pmp -CategoryNamePublishOption $nameOptionPair -Subscribe -Force
```

### Set-CMThirdPartyUpdateCategory

**Non-breaking changes**

Fixed an issue with the **PublishOption** parameter set to `FullContent`.

### Set-CMTSStep*

For example, **Set-CMTSStepApplyDataImage** and the 34 other similar cmdlets.

**Non-breaking changes**

Parameter **OperatorType** has another possible value: `NotLike`

### Set-CMSoftwareUpdateAutoDeploymentRule

**Breaking changes**

Fixed an issue for parameter **O365LanguageSelection**. You now need to specify a language with a country name. This change aligns this parameter with the options in the Configuration Manager console. For example, `-O365LanguageSelection "English (United States)"`

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To send feedback, use the Configuration Manager console. For more information, see [Feedback for PowerShell](/mem/configmgr/core/understand/product-feedback#feedback-for-powershell).
