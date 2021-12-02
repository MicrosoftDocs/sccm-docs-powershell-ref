---
title: Version 2111 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2111.
ms.date: 12/01/2021
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.localizationpriority: null
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Configuration Manager cmdlet library changes for version 2111

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2111.

> [!NOTE]
> Configuration Manager current branch version 2107 is the baseline for these changes. For more information, see [Configuration Manager cmdlet library changes for version 2107](2107-release-notes.md).

## Module changes

When you install the Configuration Manager console, the path to the **ConfigurationManager** PowerShell module is now added to the system environment variable, **PSModulePath**. For example, by default, this path is `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin`.

With this change, it's easier to import this module with the following command: `Import-Module ConfigurationManager`

For more information, see [about_PSModulePath](/powershell/module/microsoft.powershell.core/about/about_psmodulepath).

## New cmdlets

<!-- - [<cmdlet>](/powershell/module/configurationmanager/): -->
- Get-CMDeploymentTypeRequirement<!-- ](/powershell/module/configurationmanager/Get-CMDeploymentTypeRequirement) -->: Use this cmdlet to get the requirement rules for the specified deployment type. You can use the returned object to add the same rules to another deployment type.

- Remove-CMSoftwareUpdateFromPackage<!-- ](/powershell/module/configurationmanager/Remove-CMSoftwareUpdateFromPackage) -->: Use this cmdlet to remove the specified software update from a package.

- Set-CMApplicationSupersedence<!-- ](/powershell/module/configurationmanager/Set-CMApplicationSupersedence) -->: Use this cmdlet to set deployment type supersedence for the specified application. <!-- ALSO LINK IN DEPRECATED SECTION -->

### Orchestration groups

For more information about this feature, see [Orchestration groups in Configuration Manager](/mem/configmgr/sum/deploy-use/orchestration-groups).

- Get-CMOrchestrationGroup<!-- ](/powershell/module/configurationmanager/Get-CMOrchestrationGroup) -->: Use this cmdlet to get an orchestration group object by name or ID. You can use this object to start, remove, or configure the orchestration group.

- Invoke-CMOrchestrationGroup<!-- ](/powershell/module/configurationmanager/Invoke-CMOrchestrationGroup) -->: Use this cmdlet to start orchestration.

- New-CMOrchestrationGroup<!-- ](/powershell/module/configurationmanager/New-CMOrchestrationGroup) -->: Use this cmdlet to create a new orchestration group.

- Remove-CMOrchestrationGroup<!-- ](/powershell/module/configurationmanager/Remove-CMOrchestrationGroup) -->: Use this cmdlet to remove the specified orchestration group.

- Set-CMOrchestrationGroup<!-- ](/powershell/module/configurationmanager/Set-CMOrchestrationGroup) -->: Use this cmdlet to configure an orchestration group.

### Role-based administration

For more information on security roles and permissions, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

- Get-CMSecurityRolePermission<!-- ](/powershell/module/configurationmanager/Get-CMSecurityRolePermission) -->: Use this cmdlet to get the permissions for the specified security role.

- Set-CMSecurityRolePermission<!-- ](/powershell/module/configurationmanager/Set-CMSecurityRolePermission) -->: Use this cmdlet to configure a security role with specific permissions.

### Folder management

For more information on folders, see [How to use the Configuration Manager console](/mem/configmgr/core/servers/manage/admin-console#nodes).

- Get-CMFolder<!-- ](/powershell/module/configurationmanager/Get-CMFolder) -->: Use this cmdlet to get all customized folders or folders from the specified parent path.

- New-CMFolder<!-- ](/powershell/module/configurationmanager/New-CMFolder) -->: Use this cmdlet to create a new folder under the specified parent folder path.

- Remove-CMFolder<!-- ](/powershell/module/configurationmanager/Remove-CMFolder) -->: Use this cmdlet to remove the specified folder.

- Set-CMFolder<!-- ](/powershell/module/configurationmanager/Set-CMFolder) -->: Use this cmdlet to configure the specified folder. For example, rename it or move it to another folder.

## Deprecated and removed cmdlets

The following cmdlets are deprecated and may be removed in a future release:

| Deprecated cmdlet | Replacement |
|---------|---------|
| Add-CMDeploymentTypeSupersedence | Set-CMApplicationSupersedence<!-- ](/powershell/module/configurationmanager/Set-CMApplicationSupersedence) --> |
| Remove-CMDeploymentTypeSupersedence | Set-CMApplicationSupersedence<!-- ](/powershell/module/configurationmanager/Set-CMApplicationSupersedence) --> |
| Set-CMDeploymentTypeSupersedence | Set-CMApplicationSupersedence<!-- ](/powershell/module/configurationmanager/Set-CMApplicationSupersedence) --> |

The following cmdlets are no longer available because the underlying feature is no longer supported:

- Get-CMTSStepConvertDisk
- New-CMTSStepConverDisk
- Remove-CMTSStepConvertDisk
- Set-CMTSStepConvertDisk

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

### Add-CMDeviceCollectionDirectMembershipRule

For more information, see [Add-CMDeviceCollectionDirectMembershipRule](/powershell/module/configurationmanager/Add-CMDeviceCollectionDirectMembershipRule).

**Bugs that were fixed**

Fixed an issue when adding a rule by resource object.

### Add-CMDistributionPoint

**Bugs that were fixed**

You can't specify the central administration site (CAS) for the **SiteCode**  parameter, which doesn't support any client-facing site system roles.

### Get-CMClientSetting

For more information, see [Get-CMClientSetting](/powershell/module/configurationmanager/Get-CMClientSetting).

**Non-breaking changes**

Added support to return the value for the [Disable Deadline Randomization](/mem/configmgr/core/clients/deploy/about-client-settings#disable-deadline-randomization) setting in the Computer Agent group.

### Get-CMPersistentUserSettingsGroup

For more information, see [Get-CMPersistentUserSettingsGroup](/powershell/module/configurationmanager/Get-CMPersistentUserSettingsGroup).

**Bugs that were fixed**

Fixed an issue with the **Name** parameter to filter on setting groups.

### Get-CMUserDeviceAffinity

For more information, see [Get-CMUserDeviceAffinity](/powershell/module/configurationmanager/Get-CMUserDeviceAffinity).

**Non-breaking changes**

Add parameter **ShowApprovedOnly** to filter out non-approved affinities.

### New-CMBoundary

For more information, see [New-CMBoundary](/powershell/module/configurationmanager/New-CMBoundary).

**Non-breaking changes**

Added new parameter **ValueStartsWith** to support improvements to VPN boundary types.

### New-CMTSPartitionSetting

For more information, see [New-CMTSPartitionSetting](/powershell/module/configurationmanager/New-CMTSPartitionSetting).

**Non-breaking changes**

Set default value for AssignVolumeLetter.

### New-CMTSStepApplyWindowsSetting

For more information, see [New-CMTSStepApplyWindowsSetting](/powershell/module/configurationmanager/New-CMTSStepApplyWindowsSetting).

**Breaking changes**

Removed the following unsupported parameters:

- **MaximumConnection**
- **ServerLicensing**

### New-CMTSStepPrestartCheck

For more information, see [New-CMTSStepPrestartCheck](/powershell/module/configurationmanager/New-CMTSStepPrestartCheck).

**Non-breaking changes**

Added new parameters for TPM existence check:

- **CheckTpmEnabled**
- **CheckTpmActivated**

### New-CMWdacSetting

For more information, see [New-CMWdacSetting](/powershell/module/configurationmanager/New-CMWdacSetting).

**Non-breaking changes**

Added support for new platform rules for Windows 10 ARM64 and Windows 10 multi-session.

### Remove-CMPersistentUserSettingsGroup

For more information, see [Remove-CMPersistentUserSettingsGroup](/powershell/module/configurationmanager/Remove-CMPersistentUserSettingsGroup).

**Bugs that were fixed**

Fixed a query issue when remove settings group by name.

### Set-CMBoundary

For more information, see [Set-CMBoundary](/powershell/module/configurationmanager/Set-CMBoundary).

**Non-breaking changes**

Added new parameter **ValueStartsWith** to support improvements to VPN boundary types.

### Set-CMDeviceVariable

For more information, see [Set-CMDeviceVariable](/powershell/module/configurationmanager/Set-CMDeviceVariable).

**Non-breaking changes**

The parameter **VariableName** is now case-insensitive.

### Set-CMDistributionPoint

For more information, see [Set-CMDistributionPoint](/powershell/module/configurationmanager/Set-CMDistributionPoint).

**Non-breaking changes**

Added new parameter **EnableMaintenanceMode** to support to manage [maintenance mode](/mem/configmgr/core/servers/deploy/configure/install-and-configure-distribution-points#bkmk_maint).

### Set-CMSoftwareUpdatePoint

For more information, see [Set-CMSoftwareUpdatePoint](/powershell/module/configurationmanager/Set-CMSoftwareUpdatePoint).

**Bugs that were fixed**

Fixed an issue with regular expression processing when trying to clear the WSUS access account from a software update point.

### Set-CMSoftwareUpdatePointComponent

For more information, see [Set-CMSoftwareUpdatePointComponent](/powershell/module/configurationmanager/Set-CMSoftwareUpdatePointComponent).

**Breaking changes**

Removed the deprecated parameter **EnableSynchronization** from this cmdlet. To set the synchronization schedule, use the **Schedule** parameter.

For example, to disable the synchronization schedule:

```powershell
Set-CMSoftwareUpdatePointComponent -Name "Contoso-SiteSysSrv.Western.Contoso.com" -Schedule $null
```

### Set-CMTSStepApplyWindowsSetting

For more information, see [Set-CMTSStepApplyWindowsSetting](/powershell/module/configurationmanager/Set-CMTSStepApplyWindowsSetting).

**Breaking changes**

Removed the following unsupported parameters:

- **MaximumConnection**
- **ServerLicensing**

### Set-CMTSStepPrestartCheck

For more information, see [Set-CMTSStepPrestartCheck](/powershell/module/configurationmanager/Set-CMTSStepPrestartCheck).

**Non-breaking changes**

Added new parameters for TPM existence check:

- **CheckTpmEnabled**
- **CheckTpmActivated**

## Changes to multiple cmdlets

The following changes were made across multiple cmdlets of a similar type.

### Import and export verbs

This change applies to all cmdlets with `import` and `export` verbs. For example, [Import-CMAADClientApplication](/powershell/module/configurationmanager/import-cmaadclientapplication) and [Export-CMApplication](/powershell/module/configurationmanager/export-cmapplication).

**Non-breaking changes**

To allow for consistent parameter use across these cmdlets, they all have aliases for the parameter to specify the import path: `FilePath`, `FileName`, `ImportFilePath`, `Path`

### Configure application deployment types

This change applies to all cmdlets with `set` verbs to configure application deployment types. These cmdlet names use the pattern `Set-CM*DeploymentType`, where `*` is the application technology. For example, [Set-CMMsiDeploymentType](/powershell/module/configurationmanager/Set-CMMsiDeploymentType).

**Bugs that were fixed**

Fixed a requirement rule name issue with these cmdlets.

### Create requirement rules

This change applies to all cmdlets with the name pattern `New-CMRequirementRule*`, where `*` is the type of rule. For example, [New-CMRequirementRuleExistential](/powershell/module/configurationmanager/New-CMRequirementRuleExistential).

**Bugs that were fixed**

Fixed a requirement rule name issue with these cmdlets.

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To send feedback, use the Configuration Manager console. For more information, see [Feedback for PowerShell](/mem/configmgr/core/understand/product-feedback#feedback-for-powershell).

To submit new feature requests, see the PowerShell group of [Configuration Manager on UserVoice](https://configurationmanager.uservoice.com).
