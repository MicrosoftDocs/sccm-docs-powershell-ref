---
title: Version 2203 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2203.
ms.date: 03/28/2022
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.localizationpriority: null
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Configuration Manager cmdlet library changes for version 2203

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2203.

> [!NOTE]
> Configuration Manager current branch version 2111 is the baseline for these changes. For more information, see [Configuration Manager cmdlet library changes for version 2111](2111-release-notes.md).

<!--
## Module changes
 -->

## New cmdlets

<!-- - [<cmdlet>](/powershell/module/configurationmanager/): -->

- Get-CMAADTenant<!-- ](/powershell/module/configurationmanager/Get-CMAADTenant) -->: Get an Azure Active Directory (Azure AD) tenant from the site.

- Set-CMCollectionCloudSync<!-- ](/powershell/module/configurationmanager/Set-CMCollectionCloudSync) -->: Configure cloud sync features for a collection.

## Deprecated and removed cmdlets

The following cmdlets for asset intelligence are deprecated and may be removed in a future release:

- Add-CMAssetIntelligenceSynchronizationPoint
- Get-CMAssetIntelligenceProxy
- Get-CMAssetIntelligenceSynchronizationPoint
- Remove-CMAssetIntelligenceSynchronizationPoint
- Send-CMAssetIntelligenceCatalogUpdateRequest
- Set-CMAssetIntelligenceSynchronizationPoint
- Sync-CMAssetIntelligenceCatalog

<!--
The following cmdlets are deprecated and may be removed in a future release:

| Deprecated cmdlet | Replacement |
|---------|---------|

The following cmdlets are no longer available because the underlying feature is no longer supported:
-->


<!--
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

### Add-CMSoftwareUpdatePoint

For more information, see [Add-CMSoftwareUpdatePoint](/powershell/module/configurationmanager/Add-CMSoftwareUpdatePoint).

**Non-breaking changes**

Added new parameter **Wledbat** to support LEDBAT configuration for software update points.

### Get-CMDeploymentStatusDetails

For more information, see [Get-CMDeploymentStatusDetails](/powershell/module/configurationmanager/Get-CMDeploymentStatusDetails).

**Bugs that were fixed**

Updated the cmdlet to avoid a potential null reference error.

### Get-CMDeploymentTypeDetectionClause

For more information, see [Get-CMDeploymentTypeDetectionClause](/powershell/module/configurationmanager/Get-CMDeploymentTypeDetectionClause).

**Non-breaking changes**

The cmdlet can now get a detection clause from a script deployment type.

### Import-CMApplication

For more information, see [Import-CMApplication](/powershell/module/configurationmanager/Import-CMApplication).

**Non-breaking changes**

Updated the import logic to align with console. Added new warning messages.

### New-CMApplication

For more information, see [New-CMApplication](/powershell/module/configurationmanager/New-CMApplication).

**Non-breaking changes**

It can now get an application icon from the specified file.

### New-CMBoundary

For more information, see [New-CMBoundary](/powershell/module/configurationmanager/New-CMBoundary).

**Non-breaking changes**

Updated value validation for VPN boundary.

### New-CMCoManagementPolicy

For more information, see [New-CMCoManagementPolicy](/powershell/module/configurationmanager/New-CMCoManagementPolicy).

**Non-breaking changes**

The cmdlet now supports applicability for Windows 11 on ARM64 devices.

### New-CMPackage

For more information, see [New-CMPackage](/powershell/module/configurationmanager/New-CMPackage).

**Non-breaking changes**

Added parameter **IconLocationFile** to use a custom icon from the specified file. For more information, see [Custom icon support for task sequences and packages](../../technical-preview-2201.md#bkmk_tsico).

### New-CMSoftwareUpdateDeployment

For more information, see [New-CMSoftwareUpdateDeployment](/powershell/module/configurationmanager/New-CMSoftwareUpdateDeployment).

**Non-breaking changes**

Added parameter **PreDownloadUpdateContent** to support [pre-download for available software updates](../../technical-preview-2202.md#bkmk_pre-download).

### New-CMTaskSequence

For more information, see [New-CMTaskSequence](/powershell/module/configurationmanager/New-CMTaskSequence).

**Non-breaking changes**

Added the **IconLocationFile** parameter to support specifying an icon for the task sequence. For more information, see [Support for task sequence and package icons](#bkmk_tsico).

### New-CMTaskSequenceDeployment

For more information, see [New-CMTaskSequenceDeployment](/powershell/module/configurationmanager/New-CMTaskSequenceDeployment).

**Bugs that were fixed**

Fixed an issue with the **AllowSharedContent** parameter.

### Publish-CMThirdPartySoftwareUpdateContent

For more information, see [Publish-CMThirdPartySoftwareUpdateContent](/powershell/module/configurationmanager/Publish-CMThirdPartySoftwareUpdateContent).

**Non-breaking changes**

Added the **Force** parameter to run the command without asking for confirmation.

### Set-CMBoundary

For more information, see [Set-CMBoundary](/powershell/module/configurationmanager/Set-CMBoundary).

**Non-breaking changes**

Updated value validation for VPN boundary.

### Set-CMPackage

For more information, see [Set-CMPackage](/powershell/module/configurationmanager/Set-CMPackage).

**Non-breaking changes**

Added parameter **IconLocationFile** to use a custom icon from the specified file. For more information, see [Custom icon support for task sequences and packages](../../technical-preview-2201.md#bkmk_tsico).

### Set-CMSoftwareUpdateDeployment

For more information, see [Set-CMSoftwareUpdateDeployment](/powershell/module/configurationmanager/Set-CMSoftwareUpdateDeployment).

**Non-breaking changes**

Added parameter **PreDownloadUpdateContent** to support [pre-download for available software updates](../../technical-preview-2202.md#bkmk_pre-download).

### Set-CMSoftwareUpdatePoint

For more information, see [Set-CMSoftwareUpdatePoint](/powershell/module/configurationmanager/Set-CMSoftwareUpdatePoint).

**Non-breaking changes**

Added new parameter **Wledbat** to support LEDBAT configuration for software update points.

### Set-CMSoftwareUpdatePointComponent

For more information, see [Set-CMSoftwareUpdatePointComponent](/powershell/module/configurationmanager/Set-CMSoftwareUpdatePointComponent).

**Non-breaking changes**

Added the **NonWindowsUpdateMaxRuntimeMins** parameter to change the default maximum run time for non-Windows software updates.

### Set-CMTaskSequence

For more information, see [Set-CMTaskSequence](/powershell/module/configurationmanager/Set-CMTaskSequence).

**Non-breaking changes**

Added the **IconLocationFile** parameter to support specifying an icon for the task sequence. For more information, see [Support for task sequence and package icons](#bkmk_tsico).

### Set-CMTaskSequenceDeployment

For more information, see [Set-CMTaskSequenceDeployment](/powershell/module/configurationmanager/Set-CMTaskSequenceDeployment).

**Bugs that were fixed**

Fixed an issue with the **AllowSharedContent** parameter.

### Start-CMTaskSequenceDeployment

For more information, see [Start-CMTaskSequenceDeployment](/powershell/module/configurationmanager/Start-CMTaskSequenceDeployment).

**Bugs that were fixed**

Fixed an issue with the **AllowSharedContent** parameter.

## Changes to multiple cmdlets

The following folder-related cmdlets now support software update groups and deployment packages:

- [Get-CMFolder](/powershell/module/configurationmanager/get-cmfolder)
- [New-CMFolder](/powershell/module/configurationmanager/new-cmfolder)
- [Remove-CMFolder](/powershell/module/configurationmanager/remove-cmfolder)
- [Set-CMFolder](/powershell/module/configurationmanager/set-cmfolder)
- [Move-CMObject](/powershell/module/configurationmanager/move-cmobject)
- [Add-CMObjectSecurityScope](/powershell/module/configurationmanager/Add-CMObjectSecurityScope)
- [Remove-CMObjectSecurityScope](/powershell/module/configurationmanager/Remove-CMObjectSecurityScope)

<!-- For more general information, see [Added folder support for nodes in the Software Library](/mem/configmgr/core/get-started/2022/technical-preview-2202#bkmk_folder). -->

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To send feedback, use the Configuration Manager console. For more information, see [Feedback for PowerShell](/mem/configmgr/core/understand/product-feedback#feedback-for-powershell).
