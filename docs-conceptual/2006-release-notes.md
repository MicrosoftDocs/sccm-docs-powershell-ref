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

<!-- - [](../sccm-ps/ConfigurationManager/.md) -->

- [Add-CMTaskSequenceDeploymentType](../sccm-ps/ConfigurationManager/Add-CMTaskSequenceDeploymentType.md)
- [Set-CMApplicationPhasedDeployment](../sccm-ps/ConfigurationManager/Set-CMApplicationPhasedDeployment.md)
- [Set-CMSoftwareUpdatePhase](../sccm-ps/ConfigurationManager/Set-CMSoftwareUpdatePhase.md)
- [Set-CMSoftwareUpdatePhasedDeployment](../sccm-ps/ConfigurationManager/Set-CMSoftwareUpdatePhasedDeployment.md)
- [Set-CMTaskSequenceDeploymentType](../sccm-ps/ConfigurationManager/Set-CMTaskSequenceDeploymentType.md)
- [Set-CMTaskSequencePhase](../sccm-ps/ConfigurationManager/Set-CMTaskSequencePhase.md)
- [Set-CMTaskSequencePhasedDeployment](../sccm-ps/ConfigurationManager/Set-CMTaskSequencePhasedDeployment.md)

The following cmdlets are also new in this release, but the current article is a just stub. More information is coming soon.

- Copy-CMBlmSetting
- Copy-CMWdacSetting
- Get-CMBlmSetting
- Get-CMSettingDeployment
- Get-CMWdacSetting
- New-CMBLEncryptionMethodPolicy
- New-CMBLEncryptionMethodWithXts
- New-CMBlmSetting
- New-CMBMSClientConfigureCheckIntervalPolicy
- [New-CMBMSFDVEncryptionPolicy](../sccm-ps/ConfigurationManager/New-CMBMSFDVEncryptionPolicy.md)
- [New-CMBMSOSDEncryptionPolicy](../sccm-ps/ConfigurationManager/New-CMBMSOSDEncryptionPolicy.md)
- [New-CMBMSUserExemptionPolicy](../sccm-ps/ConfigurationManager/New-CMBMSUserExemptionPolicy.md)
- New-CMEnhancedPIN
- [New-CMFDVDenyWriteAccessPolicy](../sccm-ps/ConfigurationManager/New-CMFDVDenyWriteAccessPolicy.md)
- New-CMFDVHybridAccessPolicy
- [New-CMFDVPassPhrasePolicy](../sccm-ps/ConfigurationManager/New-CMFDVPassPhrasePolicy.md)
- New-CMMoreInfoUrlPolicy
- [New-CMNoOverwritePolicy](../sccm-ps/ConfigurationManager/New-CMNoOverwritePolicy.md)
- [New-CMOSPassphrase](../sccm-ps/ConfigurationManager/New-CMOSPassphrase.md)
- [New-CMPrebootRecoveryInfo](../sccm-ps/ConfigurationManager/New-CMPrebootRecoveryInfo.md)
- [New-CMRDVConfigureBDEPolicy](../sccm-ps/ConfigurationManager/New-CMRDVConfigureBDEPolicy.md)
- New-CMRDVDenyWriteAccessPolicy
- New-CMRDVHybridAccessPolicy
- [New-CMRDVPassPhrasePolicy](../sccm-ps/ConfigurationManager/New-CMRDVPassPhrasePolicy.md)
- [New-CMScCompliancePolicy](../sccm-ps/ConfigurationManager/New-CMScCompliancePolicy.md)
- New-CMSettingDeployment
- [New-CMTpmAutoResealPolicy](../sccm-ps/ConfigurationManager/New-CMTpmAutoResealPolicy.md)
- [New-CMUidPolicy](../sccm-ps/ConfigurationManager/New-CMUidPolicy.md)
- New-CMUseFddEnforcePolicy
- New-CMUseOsEnforcePolicy
- New-CMWdacSetting
- Remove-CMBlmSetting
- Remove-CMSettingDeployment
- Remove-CMWdacSetting
- Set-CMBlmPlaintextStorage
- Set-CMBlmSetting
- Set-CMSettingDeployment
- Set-CMWdacSetting

### Deprecated cmdlets

None

## Known issues

None

## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
For more information, see [](../sccm-ps/ConfigurationManager/.md).
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

### Add-CMComplianceSettingRegistryKeyValue

For more information, see [Add-CMComplianceSettingRegistryKeyValue](../sccm-ps/ConfigurationManager/Add-CMComplianceSettingRegistryKeyValue.md).

#### Non-breaking changes

You can now specify a null or empty string for the **-ExpectedValue** parameter.

### Get-CMBootImage

For more information, see [Get-CMBootImage](../sccm-ps/ConfigurationManager/Get-CMBootImage.md).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Get-CMOperatingSystemImage

For more information, see [Get-CMOperatingSystemImage](../sccm-ps/ConfigurationManager/Get-CMOperatingSystemImage.md).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Get-CMOperatingSystemInstaller

For more information, see [Get-CMOperatingSystemInstaller](../sccm-ps/ConfigurationManager/Get-CMOperatingSystemInstaller.md).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### New-CMApplicationDeployment

For more information, see [New-CMApplicationDeployment](../sccm-ps/ConfigurationManager/New-CMApplicationDeployment.md).

#### Non-breaking changes

You can now specify a deadline for an available deployment with superseding option.

### New-CMComplianceRuleValue

For more information, see [New-CMComplianceRuleValue](../sccm-ps/ConfigurationManager/New-CMComplianceRuleValue.md).

#### Non-breaking changes

You can now specify a null or empty string with the **-ExpectedValue** parameter.

### New-CMTSStepEnableBitLocker

For more information, see [New-CMTSStepEnableBitLocker](../sccm-ps/ConfigurationManager/New-CMTSStepEnableBitLocker.md).

#### Non-breaking changes

- Added a parameter to skip the step when the device doesn't have a valid TPM: **-EnableSkipWhenNoValidTpm**

- Added a parameter to specify the encryption method: **-EncryptionMethod**

### New-CMTSStepOfflineEnableBitLocker

For more information, see [New-CMTSStepOfflineEnableBitLocker](../sccm-ps/ConfigurationManager/New-CMTSStepOfflineEnableBitLocker.md).

#### Non-breaking changes

Added a parameter to specify the encryption method: **-EncryptionMethod**

### New-CMTSStepPartitionDisk

For more information, see [New-CMTSStepPartitionDisk](../sccm-ps/ConfigurationManager/New-CMTSStepPartitionDisk.md).

#### Non-breaking changes

Added a parameter to specify a disk number variable: **-DiskNumberVariable**

### New-CMTSStepPrestartCheck

For more information, see [New-CMTSStepPrestartCheck](../sccm-ps/ConfigurationManager/New-CMTSStepPrestartCheck.md).

#### Non-breaking changes

Fixed a blocking issue when you specify a value for the **-OSArchitecture** parameter.

### Remove-CMDeployment

For more information, see [Remove-CMDeployment](../sccm-ps/ConfigurationManager/Remove-CMDeployment.md).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMResource

For more information, see [Remove-CMResource](../sccm-ps/ConfigurationManager/Remove-CMResource.md).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMTaskSequenceGroup

For more information, see [Remove-CMTaskSequenceGroup](../sccm-ps/ConfigurationManager/Remove-CMTaskSequenceGroup.md).

#### Bugs that were fixed

Fixed bad disposal.

### Remove-CMTaskSequenceStep

For more information, see [Remove-CMTaskSequenceStep](../sccm-ps/ConfigurationManager/Remove-CMTaskSequenceStep.md).

#### Bugs that were fixed

Fixed bad disposal.

### Set-CMBootImage

For more information, see [Set-CMBootImage](../sccm-ps/ConfigurationManager/Set-CMBootImage.md).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMClientSetting

For more information, see [Set-CMClientSetting](../sccm-ps/ConfigurationManager/Set-CMClientSetting.md).

#### Non-breaking changes

Added a parameter to support the new restart setting: **-NoRebootEnforcement**

### Set-CMClientSettingComputerRestart

For more information, see [Set-CMClientSettingComputerRestart](../sccm-ps/ConfigurationManager/Set-CMClientSettingComputerRestart.md).

#### Non-breaking changes

Added a parameter to support the new restart setting: **-NoRebootEnforcement**

### Set-CMCloudManagementGateway

For more information, see [Set-CMCloudManagementGateway](../sccm-ps/ConfigurationManager/Set-CMCloudManagementGateway.md).

#### Non-breaking changes

Added the following parameters to support renewing the CMG server authentication certificate:

- **-ServiceCertPath**

- **-ServiceCertPassword**

- **-Force**

### Set-CMMsiDeploymentType

For more information, see [Set-CMMsiDeploymentType](../sccm-ps/ConfigurationManager/Set-CMMsiDeploymentType.md).

#### Non-breaking changes

You can now specify an empty string for the parameters **-UninstallCommand** and **-RepairCommand**.

### Set-CMOperatingSystemImage

For more information, see [Set-CMOperatingSystemImage](../sccm-ps/ConfigurationManager/Set-CMOperatingSystemImage.md).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMOperatingSystemInstaller

For more information, see [Set-CMOperatingSystemInstaller](../sccm-ps/ConfigurationManager/Set-CMOperatingSystemInstaller.md).

#### Non-breaking changes

Added a parameter to support the reload option: **-Reload**

### Set-CMScriptDeploymentType

For more information, see [Set-CMScriptDeploymentType](../sccm-ps/ConfigurationManager/Set-CMScriptDeploymentType.md).

#### Non-breaking changes

You can now specify an empty string for the parameters **-UninstallCommand** and **-RepairCommand**.

### Set-CMSoftwareUpdateAutoDeploymentRule

For more information, see [Set-CMSoftwareUpdateAutoDeploymentRule](../sccm-ps/ConfigurationManager/Set-CMSoftwareUpdateAutoDeploymentRule.md).

#### Bugs that were fixed

When you tried to use **Get-CMSoftwareUpdateAutoDeploymentRule** with the **-Fast** parameter, and then pipe that object to **Set-CMSoftwareUpdateAutoDeploymentRule**, it would break the auto deployment rule.

### Set-CMTSStepEnableBitLocker

For more information, see [Set-CMTSStepEnableBitLocker](../sccm-ps/ConfigurationManager/Set-CMTSStepEnableBitLocker.md).

#### Non-breaking changes

- Added a parameter to skip the step when the device doesn't have a valid TPM: **-EnableSkipWhenNoValidTpm**

- Added a parameter to allow you to specify the encryption method: **-EncryptionMethod**

### Set-CMTSStepOfflineEnableBitLocker

For more information, see [Set-CMTSStepOfflineEnableBitLocker](../sccm-ps/ConfigurationManager/Set-CMTSStepOfflineEnableBitLocker.md).

#### Non-breaking changes

Added a parameter to allow you to specify the encryption method: **-EncryptionMethod**

### Set-CMTSStepPartitionDisk

For more information, see [Set-CMTSStepPartitionDisk](../sccm-ps/ConfigurationManager/Set-CMTSStepPartitionDisk.md).

#### Non-breaking changes

Added a parameter to allow you to set a disk number variable: **-DiskNumberVariable**

### Set-CMTSStepPrestartCheck

For more information, see [Set-CMTSStepPrestartCheck](../sccm-ps/ConfigurationManager/Set-CMTSStepPrestartCheck.md).

#### Non-breaking changes

Fixed a blocking issue when user specified a value for the **OSArchitecture** parameter.

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To submit bug reports, use [send a smile in the Configuration Manager console](https://docs.microsoft.com/mem/configmgr/core/understand/find-help#product-feedback). For new feature requests, use [UserVoice](https://configurationmanager.uservoice.com).
