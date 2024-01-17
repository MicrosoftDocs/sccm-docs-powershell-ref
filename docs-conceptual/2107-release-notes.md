---
title: Version 2107 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2107.
ms.date: 08/02/2021
ms.topic: conceptual
ms.localizationpriority: low
ms.author: banreetkaur
author: Banreet
manager: apoorvseth
---

# Configuration Manager cmdlet library changes for version 2107

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2107.

> [!NOTE]
> Configuration Manager current branch version 2103 is the baseline for these changes. For more information, see [Configuration Manager cmdlet library changes for version 2103](2103-release-notes.md).

## New cmdlets for app deployment types

<!-- - [<cmdlet>](/powershell/module/configurationmanager/): -->

### Manage install behaviors for application deployment types

This set of new cmdlets is for application deployment type installation behavior. For more general information on the install behavior feature, see [Check for running executable files](/mem/configmgr/apps/deploy-use/check-for-running-executable-files).

#### Add-CMDeploymentTypeInstallBehavior

Use this cmdlet to add to the specified deployment type the executable files that need to close for the app install to succeed.

```powershell
$msi_dt = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"
Add-CMDeploymentTypeInstallBehavior -InputObject $msi_dt -ExeFileName "notepad.exe" -DisplayName "Notepad"
```

For more information, see [Add-CMDeploymentTypeInstallBehavior](/powershell/module/configurationmanager/Add-CMDeploymentTypeInstallBehavior).

#### Get-CMDeploymentTypeInstallBehavior

Use this cmdlet to get from the specified deployment type the list of executable files that need to close for the app install to succeed.

```powershell
$msi_dt = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"
Get-CMDeploymentTypeInstallBehavior -InputObject $msi_dt
```

For more information, see [Get-CMDeploymentTypeInstallBehavior](/powershell/module/configurationmanager/Get-CMDeploymentTypeInstallBehavior).

#### Remove-CMDeploymentTypeInstallBehavior

Use this cmdlet to remove from the specified deployment type the executable files that need to close for the app install to succeed.

```powershell
$msi_dt = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"
Remove-CMDeploymentTypeInstallBehavior -InputObject $msi_dt -ExeFileName "notepad.exe"
```

For more information, see [Remove-CMDeploymentTypeInstallBehavior](/powershell/module/configurationmanager/Remove-CMDeploymentTypeInstallBehavior).

#### Set-CMDeploymentTypeInstallBehavior

Use this cmdlet to modify the executable files that need to close for the app install to succeed.

```powershell
$msi_dt = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"
Set-CMDeploymentTypeInstallBehavior -InputObject $msi_dt -ExeFileName "notepad.exe" -NewExeFileName "calc.exe" -DisplayName "Calculator"
```

For more information, see [Set-CMDeploymentTypeInstallBehavior](/powershell/module/configurationmanager/Set-CMDeploymentTypeInstallBehavior).

### Manage return codes for application deployment types

This set of new cmdlets is for application deployment type return codes. For more general information, see [Deployment type Return Codes](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-return).

#### Add-CMDeploymentTypeReturnCode

Use this cmdlet to add return codes to a supported deployment type.

```powershell
$msi_dt = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"
Add-CMDeploymentTypeReturnCode -InputObject $msi_dt -ReturnCode 1602 -Name "User cancel" -CodeType Failure -Description "The user cancelled the installation"
```

For more information, see [Add-CMDeploymentTypeReturnCode](/powershell/module/configurationmanager/Add-CMDeploymentTypeReturnCode).

#### Get-CMDeploymentTypeReturnCode

Use this cmdlet to get the list of return codes from the specified deployment type.

```powershell
Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)" | Get-CMDeploymentTypeReturnCode
```

For more information, see [Get-CMDeploymentTypeReturnCode](/powershell/module/configurationmanager/Get-CMDeploymentTypeReturnCode).

#### Remove-CMDeploymentTypeReturnCode

Use this cmdlet to delete return codes from the specified deployment type.

```powershell
$msi_dt = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"
Remove-CMDeploymentTypeReturnCode -InputObject $msi_dt -ReturnCode 1602
```

For more information, see [Remove-CMDeploymentTypeReturnCode](/powershell/module/configurationmanager/Remove-CMDeploymentTypeReturnCode).

#### Set-CMDeploymentTypeReturnCode

Use this cmdlet to modify return codes for the specified deployment type.

```powershell
$msi_dt = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"
Add-CMDeploymentTypeReturnCode -InputObject $msi_dt -ReturnCode 3010 -Name "Always reboot" -CodeType HardReboot -Description "Change soft reboot to hard reboot"
```

For more information, see [Set-CMDeploymentTypeReturnCode](/powershell/module/configurationmanager/Set-CMDeploymentTypeReturnCode).

## Other new cmdlets

### Get-CMClientSettingDeployment

Use this cmdlet to get a deployment of a custom client settings object. You can use this object with [Remove-CMClientSettingDeployment](/powershell/module/configurationmanager/remove-cmclientsettingdeployment).

For more information on client settings, see [How to configure client settings](/mem/configmgr/core/clients/deploy/configure-client-settings).

```powershell
$clientSetting =  Get-CMClientSetting -Name "Software Center customizations"
$clientSetting | Get-CMClientSettingDeployment
```

For more information, see [Get-CMClientSettingDeployment](/powershell/module/configurationmanager/Get-CMClientSettingDeployment).

### Get-CMDeploymentTypeDetectionClause

Use this cmdlet to get the detection clauses from the specified deployment type.

You can use this cmdlet to get a detection clause from one app and apply it to another, for example:

```powershell
$appMsi = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"

$clause1 = Get-CMDeploymentTypeDetectionClause -InputObject $appMsi

Set-CMScriptDeploymentType -ApplicationName "Configuration Manager console" -DeploymentTypeName "Install" -AddDetectionClause $clause1
```

For more information, see [Get-CMDeploymentTypeDetectionClause](/powershell/module/configurationmanager/Get-CMDeploymentTypeDetectionClause).

### Get-CMPersistentUserSettingsGroup

Use this cmdlet to get the list of site-wide settings that you've stored. These settings follow you on different devices.

For example, [Configuration Manager console notifications](/mem/configmgr/core/servers/manage/admin-console-notifications) that are active or you've dismissed.

For more information, see [Get-CMPersistentUserSettingsGroup](/powershell/module/configurationmanager/Get-CMPersistentUserSettingsGroup).

### Get-CMSoftwareUpdateContentInfo

Use this cmdlet to get software update content information.

```powershell
$update = Get-CMSoftwareUpdate -ArticleId "5004237" -Fast
Get-CMSoftwareUpdateContentInfo -InputObject $update[1]
```

For more information, see [Get-CMSoftwareUpdateContentInfo](/powershell/module/configurationmanager/Get-CMSoftwareUpdateContentInfo).

### Remove-CMPersistentUserSettingsGroup

Use this cmdlet to reset your site-wide settings.

For example, you can restore [Configuration Manager console notifications](/mem/configmgr/core/servers/manage/admin-console-notifications) that you've dismissed. After you run this cmdlet, and you restart the Configuration Manager console, you'll see all available notifications again.

For more information, see [Remove-CMPersistentUserSettingsGroup](/powershell/module/configurationmanager/Remove-CMPersistentUserSettingsGroup).

## Deprecated and removed cmdlets

The following cmdlets to start a deployment are deprecated and may be removed in a future release:

| Deprecated cmdlet | Replacement |
|---------|---------|
| Start-CMApplicationDeploymentSimulation | [New-CMApplicationDeployment](/powershell/module/configurationmanager/New-CMApplicationDeployment) with the **Simulation** parameter |
| Start-CMClientSettingDeployment | [New-CMClientSettingDeployment](/powershell/module/configurationmanager/New-CMClientSettingDeployment) |
| Start-CMAntimalwarePolicyDeployment | [New-CMAntimalwarePolicyDeployment](/powershell/module/configurationmanager/New-CMAntimalwarePolicyDeployment) |

The following cmdlets are no longer available because the underlying features are no longer supported:

- Add-CMApplicationCatalogWebServicePoint
- Add-CMApplicationCatalogWebsitePoint
- Get-CMApplicationCatalogWebServicePoint
- Get-CMApplicationCatalogWebsitePoint
- Remove-CMApplicationCatalogWebServicePoint
- Remove-CMApplicationCatalogWebsitePoint
- Set-CMApplicationCatalogWebsitePoint

- Get-CMVhd
- New-CMVhd
- Remove-CMVhd
- Set-CMVhd

<!-- 
The following cmdlets are deprecated:

- [<cmdlet>](/powershell/module/configurationmanager/)

## Known issues

None
 -->

## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality or bug fixes. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
For more information, see [](/powershell/module/configurationmanager/).
**Breaking changes**
**Bugs that were fixed**
**Non-breaking changes**
-->

### Add-CMDeviceCollectionDirectMembershipRule

For more information, see [Add-CMDeviceCollectionDirectMembershipRule](/powershell/module/configurationmanager/Add-CMDeviceCollectionDirectMembershipRule).

**Bugs that were fixed**

Fixed an issue when trying to add thousands of devices as direct membership rules.

### Add-CMDistributionPoint

For more information, see [Add-CMDistributionPoint](/powershell/module/configurationmanager/Add-CMDistributionPoint).

**Breaking changes**

The default minimum free space changed from 50 MB to **500 MB**.

### Add-CMTaskSequenceStep

For more information, see [Add-CMTaskSequenceStep](/powershell/module/configurationmanager/Add-CMTaskSequenceStep).

**Non-breaking changes**

Removed unnecessary parameter **StepName**.

### Disconnect-CMTrackedObject

For more information, see [Disconnect-CMTrackedObject](/powershell/module/configurationmanager/Disconnect-CMTrackedObject).

**Non-breaking changes**

Added alias **Disconnect-CMObject** for this cmdlet.

### Get-CMApplicationGroup

For more information, see [Get-CMApplicationGroup](/powershell/module/configurationmanager/Get-CMApplicationGroup).

**Bugs that were fixed**

Fixed an issue to get the correct app group path.

### Get-CMDeploymentStatusDetails

For more information, see [Get-CMDeploymentStatusDetails](/powershell/module/configurationmanager/Get-CMDeploymentStatusDetails).

**Bugs that were fixed**

Fixed query condition to avoid potential type mismatch issue.

### Import-CMAntimalwarePolicy

For more information, see [Import-CMAntimalwarePolicy](/powershell/module/configurationmanager/Import-CMAntimalwarePolicy).

**Non-breaking changes**

Added support for audit mode policy with potentially unwanted applications. For more information, see [Audit mode for potentially unwanted applications](/mem/configmgr/core/plan-design/changes/whats-new-in-version-2107#audit-mode-for-potentially-unwanted-applications).

### Import-CMQuery

For more information, see [Import-CMQuery](/powershell/module/configurationmanager/Import-CMQuery).

**Bugs that were fixed**

Fixed an issue to unblock the import function.

### New-CMAdministrativeUser

For more information, see [New-CMAdministrativeUser](/powershell/module/configurationmanager/New-CMAdministrativeUser).

**Bugs that were fixed**

Fixed an issue when the user name is `me`.

### New-CMApplicationDeployment

For more information, see [New-CMApplicationDeployment](/powershell/module/configurationmanager/New-CMApplicationDeployment).

**Non-breaking changes**

Added the **AutoCloseExecutable** parameter to enable the application deployment setting for install behaviors.

### New-CMCloudManagementGateway

For more information, see [New-CMCloudManagementGateway](/powershell/module/configurationmanager/New-CMCloudManagementGateway).

**Breaking changes**

The **ServiceCertPassword** parameter is now required.

### New-CMMigrationJob

For more information, see [New-CMMigrationJob](/powershell/module/configurationmanager/New-CMMigrationJob).

**Bugs that were fixed**

Unblocked the migration of software distribution deployment objects.

### New-CMSecondarySite

For more information, see [New-CMSecondarySite](/powershell/module/configurationmanager/New-CMSecondarySite).

**Breaking changes**

Changed the default minimum free space from 200 MB to **500 MB**.

### New-CMSoftwareUpdateAutoDeploymentRule

For more information, see [New-CMSoftwareUpdateAutoDeploymentRule](/powershell/module/configurationmanager/New-CMSoftwareUpdateAutoDeploymentRule).

**Bugs that were fixed**

Fixed an issue with the **Product** parameter. When there are multiple products with the same name, it now selects all of them.

### New-CMSoftwareUpdateDeployment

For more information, see [New-CMSoftwareUpdateDeployment](/powershell/module/configurationmanager/New-CMSoftwareUpdateDeployment).

**Non-breaking changes**

Added **Description** alias to **Comment** parameter.

### New-CMTaskSequence

For more information, see [New-CMTaskSequence](/powershell/module/configurationmanager/New-CMTaskSequence).

**Non-breaking changes**

- Extended the maximum length of the **Description** parameter to `512` characters.

- Added new parameter **HighPerformance** to support performance setting.

- The legacy **InstallationLicensingMode** parameter was removed.

- Removed the **NewInstallOSImageVhd** parameter set.

- Removed the **InstallOperatingSystemImageVhd** parameter.

### New-CMTaskSequenceDeployment

For more information, see [New-CMTaskSequenceDeployment](/powershell/module/configurationmanager/New-CMTaskSequenceDeployment).

**Bugs that were fixed**

Fixed an issue with high-performance power plans.

### New-CMTSStepApplyDriverPackage

For more information, see [New-CMTSStepApplyDriverPackage](/powershell/module/configurationmanager/New-CMTSStepApplyDriverPackage).

**Non-breaking changes**

Added a condition to validate a package for the specified **PackageId**.

### New-CMTSStepApplyOperatingSystem

For more information, see [New-CMTSStepApplyOperatingSystem](/powershell/module/configurationmanager/New-CMTSStepApplyOperatingSystem).

**Bugs that were fixed**

Fixed validation issues with the **DestinationVariable** parameter to allow values that start with an underscore (`_`).

**Non-breaking changes**

Added the **LayeredDriver** parameter to support layered keyboard driver during OS deployment.

### New-CMTSStepUpgradeOperatingSystem

For more information, see [New-CMTSStepUpgradeOperatingSystem](/powershell/module/configurationmanager/New-CMTSStepUpgradeOperatingSystem).

**Non-breaking changes**

Added new parameter **SoftwareUpdate** to specify a feature update for the [Upgrade OS](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_UpgradeOS) task sequence step.

### Publish-CMPrestageContent

For more information, see [Publish-CMPrestageContent](/powershell/module/configurationmanager/Publish-CMPrestageContent).

**Bugs that were fixed**

Fixed potential invalid object issue.

### Remove-CMApplicationGroup

For more information, see [Remove-CMApplicationGroup](/powershell/module/configurationmanager/Remove-CMApplicationGroup).

**Bugs that were fixed**

Fixed an issue to get the correct app group path when using the pipeline.

### Set-CMAntimalwarePolicy

For more information, see [Set-CMAntimalwarePolicy](/powershell/module/configurationmanager/Set-CMAntimalwarePolicy).

**Non-breaking changes**

Added the parameter **PuaProtection** to support potentially unwanted applications.

### Set-CMApplicationDeployment

For more information, see [Set-CMApplicationDeployment](/powershell/module/configurationmanager/Set-CMApplicationDeployment).

**Non-breaking changes**

Added the **AutoCloseExecutable** parameter to enable the application deployment setting for install behaviors.

### Set-CMClientSetting

For more information, see [Set-CMClientSetting](/powershell/module/configurationmanager/Set-CMClientSetting).

**Non-breaking changes**

Added a meaningful deprecation message for the **SoftwareMetering** parameter.

### Set-CMClientSettingSoftwareUpdate

For more information, see [Set-CMClientSettingSoftwareUpdate](/powershell/module/configurationmanager/Set-CMClientSettingSoftwareUpdate).

**Non-breaking changes**

Added the parameter **EnableWsusCertPinning** to support certificate pinning.

### Set-CMDeploymentType

For more information, see [Set-CMDeploymentType](/powershell/module/configurationmanager/Set-CMDeploymentType).

**Bugs that were fixed**

Fixed an issue with the **AddRequirement** parameter to add new rules.

### Set-CMMsiDeploymentType

For more information, see [Set-CMMsiDeploymentType](/powershell/module/configurationmanager/Set-CMMsiDeploymentType).

**Bugs that were fixed**

Update the deployment type according to the installer type to avoid resetting the configurations when you change the content location.

**Non-breaking changes**

Add support for specifying a folder path to the **ContentLocation** parameter.

### Set-CMTaskSequence

For more information, see [Set-CMTaskSequence](/powershell/module/configurationmanager/Set-CMTaskSequence).

**Non-breaking changes**

Added new parameter **HighPerformance** to support performance setting for task sequence.

### Set-CMTSStepApplyDriverPackage

For more information, see [Set-CMTSStepApplyDriverPackage](/powershell/module/configurationmanager/Set-CMTSStepApplyDriverPackage).

**Non-breaking changes**

Added a condition to validate a package for the specified **PackageId**.

### Set-CMTSStepApplyOperatingSystem

For more information, see [Set-CMTSStepApplyOperatingSystem](/powershell/module/configurationmanager/Set-CMTSStepApplyOperatingSystem).

**Bugs that were fixed**

Fixed an issue with the **Destination** parameter.

**Non-breaking changes**

Added the **LayeredDriver** parameter to support layered keyboard driver during OS deployment.

### Set-CMTSStepUpgradeOperatingSystem

For more information, see [Set-CMTSStepUpgradeOperatingSystem](/powershell/module/configurationmanager/Set-CMTSStepUpgradeOperatingSystem).

**Non-breaking changes**

Added new parameter **SoftwareUpdate** to specify a feature update for the [Upgrade OS](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_UpgradeOS) task sequence step.

### Start-CMDistributionPointUpgrade

For more information, see [Start-CMDistributionPointUpgrade](/powershell/module/configurationmanager/Start-CMDistributionPointUpgrade).

**Breaking changes**

Set the default minimum free space to **500 MB**.

### Update-CMDistributionPoint

For more information, see [Update-CMDistributionPoint](/powershell/module/configurationmanager/Update-CMDistributionPoint).

**Bugs that were fixed**

Fixed an issue to update content from both install and uninstall folders when they're different.

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To send feedback, use the Configuration Manager console. For more information, see [Feedback for PowerShell](/mem/configmgr/core/understand/product-feedback#feedback-for-powershell).
