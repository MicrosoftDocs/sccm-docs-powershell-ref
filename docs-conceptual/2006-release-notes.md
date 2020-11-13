---
title: Version 2006 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2006. 
ms.date: 08/20/2020
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Configuration Manager cmdlet library changes for version 2006

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2006.

> [!NOTE]  
> Configuration Manager current branch version 2002 is the baseline for these changes. For more information, see [Configuration Manager cmdlet library changes for version 2002](2002-release-notes.md).

## Important changes

### New cmdlets

<!-- - [<cmdlet>](/powershell/module/configurationmanager/<cmdlet>) -->

- [Add-CMTaskSequenceDeploymentType](/powershell/module/configurationmanager/add-cmtasksequencedeploymenttype)
- [Set-CMApplicationPhasedDeployment](/powershell/module/configurationmanager/set-cmapplicationphaseddeployment)
- [Set-CMSoftwareUpdatePhase](/powershell/module/configurationmanager/set-cmsoftwareupdatephase)
- [Set-CMSoftwareUpdatePhasedDeployment](/powershell/module/configurationmanager/set-cmsoftwareupdatephaseddeployment)
- [Set-CMTaskSequenceDeploymentType](/powershell/module/configurationmanager/set-cmtasksequencedeploymenttype)
- [Set-CMTaskSequencePhase](/powershell/module/configurationmanager/set-cmtasksequencephase)
- [Set-CMTaskSequencePhasedDeployment](/powershell/module/configurationmanager/set-cmtasksequencephaseddeployment)

Use the following cmdlets to configure BitLocker management policies:

- [New-CMBLEncryptionMethodPolicy](/powershell/module/configurationmanager/new-cmblencryptionmethodpolicy)
- [New-CMBLEncryptionMethodWithXts](/powershell/module/configurationmanager/new-cmblencryptionmethodwithxts)
- [New-CMBMSClientConfigureCheckIntervalPolicy](/powershell/module/configurationmanager/new-cmbmsclientconfigurecheckintervalpolicy)
- [New-CMBMSFDVEncryptionPolicy](/powershell/module/configurationmanager/new-cmbmsfdvencryptionpolicy)
- [New-CMBMSOSDEncryptionPolicy](/powershell/module/configurationmanager/new-cmbmsosdencryptionpolicy)
- [New-CMBMSUserExemptionPolicy](/powershell/module/configurationmanager/new-cmbmsuserexemptionpolicy)
- [New-CMEnhancedPIN](/powershell/module/configurationmanager/new-cmenhancedpin)
- [New-CMFDVDenyWriteAccessPolicy](/powershell/module/configurationmanager/new-cmfdvdenywriteaccesspolicy)
- [New-CMFDVPassPhrasePolicy](/powershell/module/configurationmanager/new-cmfdvpassphrasepolicy)
- [New-CMMoreInfoUrlPolicy](/powershell/module/configurationmanager/new-cmmoreinfourlpolicy)
- [New-CMNoOverwritePolicy](/powershell/module/configurationmanager/new-cmnooverwritepolicy)
- [New-CMOSPassphrase](/powershell/module/configurationmanager/new-cmospassphrase)
- [New-CMPrebootRecoveryInfo](/powershell/module/configurationmanager/new-cmprebootrecoveryinfo)
- [New-CMRDVConfigureBDEPolicy](/powershell/module/configurationmanager/new-cmrdvconfigurebdepolicy)
- [New-CMRDVDenyWriteAccessPolicy](/powershell/module/configurationmanager/new-cmrdvdenywriteaccesspolicy)
- [New-CMRDVPassPhrasePolicy](/powershell/module/configurationmanager/new-cmrdvpassphrasepolicy)
- [New-CMScCompliancePolicy](/powershell/module/configurationmanager/new-cmsccompliancepolicy)
- [New-CMTpmAutoResealPolicy](/powershell/module/configurationmanager/new-cmtpmautoresealpolicy)
- [New-CMUidPolicy](/powershell/module/configurationmanager/new-cmuidpolicy)
- [New-CMUseFddEnforcePolicy](/powershell/module/configurationmanager/new-cmusefddenforcepolicy)
- [New-CMUseOsEnforcePolicy](/powershell/module/configurationmanager/new-cmuseosenforcepolicy)
- [Set-CMBlmPlaintextStorage](/powershell/module/configurationmanager/set-cmblmplaintextstorage)

Use the following cmdlets to manage BitLocker management policy settings objects:

- [Copy-CMBlmSetting](/powershell/module/configurationmanager/copy-cmblmsetting)
- [Get-CMBlmSetting](/powershell/module/configurationmanager/get-cmblmsetting)
- [New-CMBlmSetting](/powershell/module/configurationmanager/new-cmblmsetting)
- [Remove-CMBlmSetting](/powershell/module/configurationmanager/remove-cmblmsetting)
- [Set-CMBlmSetting](/powershell/module/configurationmanager/set-cmblmsetting)

Use the following cmdlets to manage Microsoft Defender Application Control policy objects:

- [Copy-CMWdacSetting](/powershell/module/configurationmanager/copy-cmwdacsetting)
- [Get-CMWdacSetting](/powershell/module/configurationmanager/get-cmwdacsetting)
- [New-CMWdacSetting](/powershell/module/configurationmanager/new-cmwdacsetting)
- [Remove-CMWdacSetting](/powershell/module/configurationmanager/remove-cmwdacsetting)
- [Set-CMWdacSetting](/powershell/module/configurationmanager/set-cmwdacsetting)

Use the following cmdlets to manage deployments for BitLocker management policy settings and Microsoft Defender Application Control policy objects:

- [Get-CMSettingDeployment](/powershell/module/configurationmanager/get-cmsettingdeployment)
- [New-CMSettingDeployment](/powershell/module/configurationmanager/new-cmsettingdeployment)
- [Remove-CMSettingDeployment](/powershell/module/configurationmanager/remove-cmsettingdeployment)
- [Set-CMSettingDeployment](/powershell/module/configurationmanager/set-cmsettingdeployment)

### Deprecated cmdlets

None

## Known issues

None

## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
For more information, see [](/powershell/module/configurationmanager/<cmdlet>).
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

### Add-CMComplianceSettingRegistryKeyValue

For more information, see [Add-CMComplianceSettingRegistryKeyValue](/powershell/module/configurationmanager/add-cmcompliancesettingregistrykeyvalue).

#### Non-breaking changes

You can now specify a null or empty string for the **-ExpectedValue** parameter.

### Get-CMBootImage

For more information, see [Get-CMBootImage](/powershell/module/configurationmanager/get-cmbootimage).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Get-CMOperatingSystemImage

For more information, see [Get-CMOperatingSystemImage](/powershell/module/configurationmanager/get-cmoperatingsystemimage).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Get-CMOperatingSystemInstaller

For more information, see [Get-CMOperatingSystemInstaller](/powershell/module/configurationmanager/get-cmoperatingsysteminstaller).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### New-CMApplicationDeployment

For more information, see [New-CMApplicationDeployment](/powershell/module/configurationmanager/new-cmapplicationdeployment).

#### Non-breaking changes

You can now specify a deadline for an available deployment with superseding option.

### New-CMComplianceRuleValue

For more information, see [New-CMComplianceRuleValue](/powershell/module/configurationmanager/new-cmcompliancerulevalue).

#### Non-breaking changes

You can now specify a null or empty string with the **-ExpectedValue** parameter.

### New-CMTSStepEnableBitLocker

For more information, see [New-CMTSStepEnableBitLocker](/powershell/module/configurationmanager/new-cmtsstepenablebitlocker).

#### Non-breaking changes

- Added a parameter to skip the step when the device doesn't have a valid TPM: **-EnableSkipWhenNoValidTpm**

- Added a parameter to specify the encryption method: **-EncryptionMethod**

### New-CMTSStepOfflineEnableBitLocker

For more information, see [New-CMTSStepOfflineEnableBitLocker](/powershell/module/configurationmanager/new-cmtsstepofflineenablebitlocker).

#### Non-breaking changes

Added a parameter to specify the encryption method: **-EncryptionMethod**

### New-CMTSStepPartitionDisk

For more information, see [New-CMTSStepPartitionDisk](/powershell/module/configurationmanager/new-cmtssteppartitiondisk).

#### Non-breaking changes

Added a parameter to specify a disk number variable: **-DiskNumberVariable**

### New-CMTSStepPrestartCheck

For more information, see [New-CMTSStepPrestartCheck](/powershell/module/configurationmanager/new-cmtsstepprestartcheck).

#### Non-breaking changes

Fixed a blocking issue when you specify a value for the **-OSArchitecture** parameter.

### Remove-CMDeployment

For more information, see [Remove-CMDeployment](/powershell/module/configurationmanager/remove-cmdeployment).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMResource

For more information, see [Remove-CMResource](/powershell/module/configurationmanager/remove-cmresource).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMTaskSequenceGroup

For more information, see [Remove-CMTaskSequenceGroup](/powershell/module/configurationmanager/remove-cmtasksequencegroup).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMTaskSequenceStep

For more information, see [Remove-CMTaskSequenceStep](/powershell/module/configurationmanager/remove-cmtasksequencestep).

#### Bugs that were fixed

Fixed bad disposal.

### Set-CMBootImage

For more information, see [Set-CMBootImage](/powershell/module/configurationmanager/set-cmbootimage).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMClientSetting

For more information, see [Set-CMClientSetting](/powershell/module/configurationmanager/set-cmclientsetting).

#### Non-breaking changes

Added a parameter to support the new restart setting: **-NoRebootEnforcement**

### Set-CMClientSettingComputerRestart

For more information, see [Set-CMClientSettingComputerRestart](/powershell/module/configurationmanager/set-cmclientsettingcomputerrestart).

#### Non-breaking changes

Added a parameter to support the new restart setting: **-NoRebootEnforcement**

### Set-CMCloudManagementGateway

For more information, see [Set-CMCloudManagementGateway](/powershell/module/configurationmanager/set-cmcloudmanagementgateway).

#### Non-breaking changes

Added the following parameters to support renewing the CMG server authentication certificate:

- **-ServiceCertPath**

- **-ServiceCertPassword**

- **-Force**

### Set-CMMsiDeploymentType

For more information, see [Set-CMMsiDeploymentType](/powershell/module/configurationmanager/set-cmmsideploymenttype).

#### Non-breaking changes

You can now specify an empty string for the parameters **-UninstallCommand** and **-RepairCommand**.

### Set-CMOperatingSystemImage

For more information, see [Set-CMOperatingSystemImage](/powershell/module/configurationmanager/set-cmoperatingsystemimage).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMOperatingSystemInstaller

For more information, see [Set-CMOperatingSystemInstaller](/powershell/module/configurationmanager/set-cmoperatingsysteminstaller).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMScriptDeploymentType

For more information, see [Set-CMScriptDeploymentType](/powershell/module/configurationmanager/set-cmscriptdeploymenttype).

#### Non-breaking changes

You can now specify an empty string for the parameters **-UninstallCommand** and **-RepairCommand**.

### Set-CMSoftwareUpdateAutoDeploymentRule

For more information, see [Set-CMSoftwareUpdateAutoDeploymentRule](/powershell/module/configurationmanager/set-cmsoftwareupdateautodeploymentrule).

#### Bugs that were fixed

When you tried to use **Get-CMSoftwareUpdateAutoDeploymentRule** with the **-Fast** parameter, and then pipe that object to **Set-CMSoftwareUpdateAutoDeploymentRule**, it would break the auto deployment rule.

### Set-CMTSStepEnableBitLocker

For more information, see [Set-CMTSStepEnableBitLocker](/powershell/module/configurationmanager/set-cmtsstepenablebitlocker).

#### Non-breaking changes

- Added a parameter to skip the step when the device doesn't have a valid TPM: **-EnableSkipWhenNoValidTpm**

- Added a parameter to allow you to specify the encryption method: **-EncryptionMethod**

### Set-CMTSStepOfflineEnableBitLocker

For more information, see [Set-CMTSStepOfflineEnableBitLocker](/powershell/module/configurationmanager/set-cmtsstepofflineenablebitlocker).

#### Non-breaking changes

Added a parameter to allow you to specify the encryption method: **-EncryptionMethod**

### Set-CMTSStepPartitionDisk

For more information, see [Set-CMTSStepPartitionDisk](/powershell/module/configurationmanager/set-cmtssteppartitiondisk).

#### Non-breaking changes

Added a parameter to allow you to set a disk number variable: **-DiskNumberVariable**

### Set-CMTSStepPrestartCheck

For more information, see [Set-CMTSStepPrestartCheck](/powershell/module/configurationmanager/set-cmtsstepprestartcheck).

#### Non-breaking changes

Fixed a blocking issue when user specified a value for the **OSArchitecture** parameter.

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To submit bug reports, use [send a smile in the Configuration Manager console](/mem/configmgr/core/understand/find-help#product-feedback). For new feature requests, use [UserVoice](https://configurationmanager.uservoice.com).
