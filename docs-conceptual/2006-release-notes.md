---
title: Version 2006 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2006. 
ms.date: 07/31/2020
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

<!-- - [<cmdlet>](/powershell/module/configurationmanager/<cmdlet>?view=sccm-ps) -->

- [Add-CMTaskSequenceDeploymentType](/powershell/module/configurationmanager/add-cmtasksequencedeploymenttype?view=sccm-ps)
- [Set-CMApplicationPhasedDeployment](/powershell/module/configurationmanager/set-cmapplicationphaseddeployment?view=sccm-ps)
- [Set-CMSoftwareUpdatePhase](/powershell/module/configurationmanager/set-cmsoftwareupdatephase?view=sccm-ps)
- [Set-CMSoftwareUpdatePhasedDeployment](/powershell/module/configurationmanager/set-cmsoftwareupdatephaseddeployment?view=sccm-ps)
- [Set-CMTaskSequenceDeploymentType](/powershell/module/configurationmanager/set-cmtasksequencedeploymenttype?view=sccm-ps)
- [Set-CMTaskSequencePhase](/powershell/module/configurationmanager/set-cmtasksequencephase?view=sccm-ps)
- [Set-CMTaskSequencePhasedDeployment](/powershell/module/configurationmanager/set-cmtasksequencephaseddeployment?view=sccm-ps)

Use the following cmdlets to configure BitLocker management policies:

- Copy-CMBlmSetting
- Copy-CMWdacSetting
- [Get-CMBlmSetting](/powershell/module/configurationmanager/get-cmblmsetting?view=sccm-ps)
- [Get-CMSettingDeployment](/powershell/module/configurationmanager/get-cmsettingdeployment?view=sccm-ps)
- [Get-CMWdacSetting](/powershell/module/configurationmanager/get-cmwdacsetting?view=sccm-ps)
- [New-CMBLEncryptionMethodPolicy](/powershell/module/configurationmanager/new-cmblencryptionmethodpolicy?view=sccm-ps)
- [New-CMBLEncryptionMethodWithXts](/powershell/module/configurationmanager/new-cmblencryptionmethodwithxts?view=sccm-ps)
- [New-CMBlmSetting](/powershell/module/configurationmanager/new-cmblmsetting?view=sccm-ps)
- [New-CMBMSClientConfigureCheckIntervalPolicy](/powershell/module/configurationmanager/new-cmbmsclientconfigurecheckintervalpolicy?view=sccm-ps)
- [New-CMBMSFDVEncryptionPolicy](/powershell/module/configurationmanager/new-cmbmsfdvencryptionpolicy?view=sccm-ps)
- [New-CMBMSOSDEncryptionPolicy](/powershell/module/configurationmanager/new-cmbmsosdencryptionpolicy?view=sccm-ps)
- [New-CMBMSUserExemptionPolicy](/powershell/module/configurationmanager/new-cmbmsuserexemptionpolicy?view=sccm-ps)
- [New-CMEnhancedPIN](/powershell/module/configurationmanager/new-cmenhancedpin?view=sccm-ps)
- [New-CMFDVDenyWriteAccessPolicy](/powershell/module/configurationmanager/new-cmfdvdenywriteaccesspolicy?view=sccm-ps)
- [New-CMFDVPassPhrasePolicy](/powershell/module/configurationmanager/new-cmfdvpassphrasepolicy?view=sccm-ps)
- [New-CMMoreInfoUrlPolicy](/powershell/module/configurationmanager/new-cmmoreinfourlpolicy?view=sccm-ps)
- [New-CMNoOverwritePolicy](/powershell/module/configurationmanager/new-cmnooverwritepolicy?view=sccm-ps)
- [New-CMOSPassphrase](/powershell/module/configurationmanager/new-cmospassphrase?view=sccm-ps)
- [New-CMPrebootRecoveryInfo](/powershell/module/configurationmanager/new-cmprebootrecoveryinfo?view=sccm-ps)
- [New-CMRDVConfigureBDEPolicy](/powershell/module/configurationmanager/new-cmrdvconfigurebdepolicy?view=sccm-ps)
- [New-CMRDVDenyWriteAccessPolicy](/powershell/module/configurationmanager/new-cmrdvdenywriteaccesspolicy?view=sccm-ps)
- [New-CMRDVPassPhrasePolicy](/powershell/module/configurationmanager/new-cmrdvpassphrasepolicy?view=sccm-ps)
- [New-CMScCompliancePolicy](/powershell/module/configurationmanager/new-cmsccompliancepolicy?view=sccm-ps)
- [New-CMSettingDeployment](/powershell/module/configurationmanager/new-cmsettingdeployment?view=sccm-ps)
- [New-CMTpmAutoResealPolicy](/powershell/module/configurationmanager/new-cmtpmautoresealpolicy?view=sccm-ps)
- [New-CMUidPolicy](/powershell/module/configurationmanager/new-cmuidpolicy?view=sccm-ps)
- [New-CMUseFddEnforcePolicy](/powershell/module/configurationmanager/new-cmusefddenforcepolicy?view=sccm-ps)
- [New-CMUseOsEnforcePolicy](/powershell/module/configurationmanager/new-cmuseosenforcepolicy?view=sccm-ps)
- [New-CMWdacSetting](/powershell/module/configurationmanager/new-cmwdacsetting?view=sccm-ps)
- [Remove-CMBlmSetting](/powershell/module/configurationmanager/remove-cmblmsetting?view=sccm-ps)
- [Remove-CMSettingDeployment](/powershell/module/configurationmanager/remove-cmsettingdeployment?view=sccm-ps)
- Remove-CMWdacSetting
- Set-CMBlmPlaintextStorage
- [Set-CMBlmSetting](/powershell/module/configurationmanager/set-cmblmsetting?view=sccm-ps)
- [Set-CMSettingDeployment](/powershell/module/configurationmanager/set-cmsettingdeployment?view=sccm-ps)
- [Set-CMWdacSetting](/powershell/module/configurationmanager/set-cmwdacsetting?view=sccm-ps)

### Deprecated cmdlets

None

## Known issues

None

## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
For more information, see [](/powershell/module/configurationmanager/<cmdlet>?view=sccm-ps).
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

### Add-CMComplianceSettingRegistryKeyValue

For more information, see [Add-CMComplianceSettingRegistryKeyValue](/powershell/module/configurationmanager/add-cmcompliancesettingregistrykeyvalue?view=sccm-ps).

#### Non-breaking changes

You can now specify a null or empty string for the **-ExpectedValue** parameter.

### Get-CMBootImage

For more information, see [Get-CMBootImage](/powershell/module/configurationmanager/get-cmbootimage?view=sccm-ps).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Get-CMOperatingSystemImage

For more information, see [Get-CMOperatingSystemImage](/powershell/module/configurationmanager/get-cmoperatingsystemimage?view=sccm-ps).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Get-CMOperatingSystemInstaller

For more information, see [Get-CMOperatingSystemInstaller](/powershell/module/configurationmanager/get-cmoperatingsysteminstaller?view=sccm-ps).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### New-CMApplicationDeployment

For more information, see [New-CMApplicationDeployment](/powershell/module/configurationmanager/new-cmapplicationdeployment?view=sccm-ps).

#### Non-breaking changes

You can now specify a deadline for an available deployment with superseding option.

### New-CMComplianceRuleValue

For more information, see [New-CMComplianceRuleValue](/powershell/module/configurationmanager/new-cmcompliancerulevalue?view=sccm-ps).

#### Non-breaking changes

You can now specify a null or empty string with the **-ExpectedValue** parameter.

### New-CMTSStepEnableBitLocker

For more information, see [New-CMTSStepEnableBitLocker](/powershell/module/configurationmanager/new-cmtsstepenablebitlocker?view=sccm-ps).

#### Non-breaking changes

- Added a parameter to skip the step when the device doesn't have a valid TPM: **-EnableSkipWhenNoValidTpm**

- Added a parameter to specify the encryption method: **-EncryptionMethod**

### New-CMTSStepOfflineEnableBitLocker

For more information, see [New-CMTSStepOfflineEnableBitLocker](/powershell/module/configurationmanager/new-cmtsstepofflineenablebitlocker?view=sccm-ps).

#### Non-breaking changes

Added a parameter to specify the encryption method: **-EncryptionMethod**

### New-CMTSStepPartitionDisk

For more information, see [New-CMTSStepPartitionDisk](/powershell/module/configurationmanager/new-cmtssteppartitiondisk?view=sccm-ps).

#### Non-breaking changes

Added a parameter to specify a disk number variable: **-DiskNumberVariable**

### New-CMTSStepPrestartCheck

For more information, see [New-CMTSStepPrestartCheck](/powershell/module/configurationmanager/new-cmtsstepprestartcheck?view=sccm-ps).

#### Non-breaking changes

Fixed a blocking issue when you specify a value for the **-OSArchitecture** parameter.

### Remove-CMDeployment

For more information, see [Remove-CMDeployment](/powershell/module/configurationmanager/remove-cmdeployment?view=sccm-ps).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMResource

For more information, see [Remove-CMResource](/powershell/module/configurationmanager/remove-cmresource?view=sccm-ps).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMTaskSequenceGroup

For more information, see [Remove-CMTaskSequenceGroup](/powershell/module/configurationmanager/remove-cmtasksequencegroup?view=sccm-ps).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMTaskSequenceStep

For more information, see [Remove-CMTaskSequenceStep](/powershell/module/configurationmanager/remove-cmtasksequencestep?view=sccm-ps).

#### Bugs that were fixed

Fixed bad disposal.

### Set-CMBootImage

For more information, see [Set-CMBootImage](/powershell/module/configurationmanager/set-cmbootimage?view=sccm-ps).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMClientSetting

For more information, see [Set-CMClientSetting](/powershell/module/configurationmanager/set-cmclientsetting?view=sccm-ps).

#### Non-breaking changes

Added a parameter to support the new restart setting: **-NoRebootEnforcement**

### Set-CMClientSettingComputerRestart

For more information, see [Set-CMClientSettingComputerRestart](/powershell/module/configurationmanager/set-cmclientsettingcomputerrestart?view=sccm-ps).

#### Non-breaking changes

Added a parameter to support the new restart setting: **-NoRebootEnforcement**

### Set-CMCloudManagementGateway

For more information, see [Set-CMCloudManagementGateway](/powershell/module/configurationmanager/set-cmcloudmanagementgateway?view=sccm-ps).

#### Non-breaking changes

Added the following parameters to support renewing the CMG server authentication certificate:

- **-ServiceCertPath**

- **-ServiceCertPassword**

- **-Force**

### Set-CMMsiDeploymentType

For more information, see [Set-CMMsiDeploymentType](/powershell/module/configurationmanager/set-cmmsideploymenttype?view=sccm-ps).

#### Non-breaking changes

You can now specify an empty string for the parameters **-UninstallCommand** and **-RepairCommand**.

### Set-CMOperatingSystemImage

For more information, see [Set-CMOperatingSystemImage](/powershell/module/configurationmanager/set-cmoperatingsystemimage?view=sccm-ps).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMOperatingSystemInstaller

For more information, see [Set-CMOperatingSystemInstaller](/powershell/module/configurationmanager/set-cmoperatingsysteminstaller?view=sccm-ps).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMScriptDeploymentType

For more information, see [Set-CMScriptDeploymentType](/powershell/module/configurationmanager/set-cmscriptdeploymenttype?view=sccm-ps).

#### Non-breaking changes

You can now specify an empty string for the parameters **-UninstallCommand** and **-RepairCommand**.

### Set-CMSoftwareUpdateAutoDeploymentRule

For more information, see [Set-CMSoftwareUpdateAutoDeploymentRule](/powershell/module/configurationmanager/set-cmsoftwareupdateautodeploymentrule?view=sccm-ps).

#### Bugs that were fixed

When you tried to use **Get-CMSoftwareUpdateAutoDeploymentRule** with the **-Fast** parameter, and then pipe that object to **Set-CMSoftwareUpdateAutoDeploymentRule**, it would break the auto deployment rule.

### Set-CMTSStepEnableBitLocker

For more information, see [Set-CMTSStepEnableBitLocker](/powershell/module/configurationmanager/set-cmtsstepenablebitlocker?view=sccm-ps).

#### Non-breaking changes

- Added a parameter to skip the step when the device doesn't have a valid TPM: **-EnableSkipWhenNoValidTpm**

- Added a parameter to allow you to specify the encryption method: **-EncryptionMethod**

### Set-CMTSStepOfflineEnableBitLocker

For more information, see [Set-CMTSStepOfflineEnableBitLocker](/powershell/module/configurationmanager/set-cmtsstepofflineenablebitlocker?view=sccm-ps).

#### Non-breaking changes

Added a parameter to allow you to specify the encryption method: **-EncryptionMethod**

### Set-CMTSStepPartitionDisk

For more information, see [Set-CMTSStepPartitionDisk](/powershell/module/configurationmanager/set-cmtssteppartitiondisk?view=sccm-ps).

#### Non-breaking changes

Added a parameter to allow you to set a disk number variable: **-DiskNumberVariable**

### Set-CMTSStepPrestartCheck

For more information, see [Set-CMTSStepPrestartCheck](/powershell/module/configurationmanager/set-cmtsstepprestartcheck?view=sccm-ps).

#### Non-breaking changes

Fixed a blocking issue when user specified a value for the **OSArchitecture** parameter.

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To submit bug reports, use [send a smile in the Configuration Manager console](/mem/configmgr/core/understand/find-help#product-feedback). For new feature requests, use [UserVoice](https://configurationmanager.uservoice.com).
