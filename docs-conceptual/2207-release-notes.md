---
title: Version 2207 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2207.
ms.date: 08/01/2022
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.localizationpriority: null
author: banreet
ms.author: banreetkaur
manager: apoorvseth
---

# Configuration Manager cmdlet library changes for version 2207

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2207

> [!NOTE]
> Configuration Manager current branch version 2111 is the baseline for these changes. For more information, see [Configuration Manager cmdlet library changes for version 2111](2111-release-notes.md).

<!--
## Module changes
 -->

## New cmdlets

<!-- - [<cmdlet>](/powershell/module/configurationmanager/): -->

<!--Orchestration Group script cmdlets -->
### Approve-CMOrchestrationGroupScript

Use this cmdlet to approve an orchestration group script. For more information, see [About orchestration groups in Configuration Manager](https://docs.microsoft.com/en-us/mem/configmgr/sum/deploy-use/orchestration-groups).

```powershell
$referenceOG = Get-CMOrchestrationGroup -Name $Script:OGName
$preScript = $referenceOG | Get-CMOrchestrationGroupScript -ScriptType Pre
$preScript | Approve-CMOrchestrationGroupScript -Comment "Approve"
Approve-CMOrchestrationGroupScript -ScriptGuid $PreScript.ScriptGuid
```
### Deny-CMOrchestrationGroupScript

Use this cmdlet to deny an orchestration group script. For more information, see [About orchestration groups in Configuration Manager](https://docs.microsoft.com/en-us/mem/configmgr/sum/deploy-use/orchestration-groups).

```powershell
$referenceOG = Get-CMOrchestrationGroup -Name $Script:OGName
$preScript = $referenceOG | Get-CMOrchestrationGroupScript -ScriptType Pre
$preScript | Deny-CMOrchestrationGroupScript -Comment "Deny"
Deny-CMOrchestrationGroupScript -ScriptGuid $PreScript.ScriptGuid -Comment "Deny"
```

### Get-CMOrchestrationGroupScript

Use this cmdlet to get a script from the specified orchestration group. For more information, see [About orchestration groups in Configuration Manager](https://docs.microsoft.com/en-us/mem/configmgr/sum/deploy-use/orchestration-groups).

```powershell
$referenceOG = Get-CMOrchestrationGroup -Name $Script:OGName
$preScript = $referenceOG | Get-CMOrchestrationGroupScript -ScriptType Pre
```
<!--CMDPMigration script cmdlets -->
### Start-CMDPMigration

Use this cmdlet to start migration from source distribution point to destination distribution point. For more information, see [About migration in Configuration Manager](https://docs.microsoft.com/en-us/mem/configmgr/core/migration/planning-a-migration-job-strategy).

```powershell
Start-CMDPMigration -SourceDistributionPointName sourceServer.dp -DestinationDistributionPointName destinationServer.dp -LockSourceDP 1
```

### Stop-CMDPMigration

Use this cmdlet to stop migration from source distribution point to destination distribution point. For more information, see [About migration in Configuration Manager](https://docs.microsoft.com/en-us/mem/configmgr/core/migration/planning-a-migration-job-strategy).

```powershell
Stop-CMDPMigration -SourceDistributionPointName sourceServer.dp -DestinationDistributionPointName destinationServer.dp -LockSourceDP 1
```

### Get-CMDPMigrationContentStatus

Use this cmdlet to get the content status of the migration from source distribution point to destination distribution point. For more information, see [About migration in Configuration Manager](https://docs.microsoft.com/en-us/mem/configmgr/core/migration/planning-a-migration-job-strategy).

```powershell
Get-CMDPMigrationContentStatus  -SourceDistributionPointName sourceServer.dp -DestinationDistributionPointName destinationServer.dp
```

### Get-CMDPMigrationStatus

Use this cmdlet to get the status of the migration from source distribution point to destination distribution point. For more information, see [About migration in Configuration Manager](https://docs.microsoft.com/en-us/mem/configmgr/core/migration/planning-a-migration-job-strategy).

```powershell
Get-CMDPMigrationStatus -SourceDistributionPointName sourceServer.dp -DestinationDistributionPointName destinationServer.dp
```
<!--CMTrustedRootCertificationAuthority script cmdlets -->
### Get-CMTrustedRootCertificationAuthority

Use this cmdlet to get the certificates for trusted root certification authorities from the site.

```powershell
$ci =Get-CMTrustedRootCertificationAuthority
$ci =Get-CMTrustedRootCertificationAuthority -ViewDetail
```
<!--CMAAD Client and server application script cmdlets -->
### New-CMAADClientApplication

Use this cmdlet to create a client app registration in Azure Active Directory (Azure AD). When you run this cmdlet, it will prompt you to sign in to your tenant. For more information on this app registration, see [Manually register Azure AD apps for the CMG](https://docs.microsoft.com/en-us/mem/configmgr/core/clients/manage/cmg/manually-register-azure-ad-apps).

```powershell
$serverApp = New-CMAADServerApplication -AppName $appName
New-CMAADClientApplication -AppName $name -InputObject $serverApp
```

### New-CMAADServerApplication

Use this cmdlet to create a server app registration in Azure AD. When you run this cmdlet, it will prompt you to sign in to your tenant. For more information on this app registration, see [Manually register Azure AD apps for the CMG](https://docs.microsoft.com/en-us/mem/configmgr/core/clients/manage/cmg/manually-register-azure-ad-apps).

```powershell
New-CMAADServerApplication -AppName $appName
```
<!--CMAAD default boundary group script cmdlets -->
### Set-CMDefaultBoundaryGroup

Use this cmdlet to modify the properties of a default site boundary group. You can set the options to include and prefer the cloud-based sources for the clients in default site boundary group. For more information on boundary groups, see [About boundary groups in Configuration Manager](https://docs.microsoft.com/en-us/mem/configmgr/core/servers/deploy/configure/boundary-groups). 

```powershell
Set-CMDefaultBoundaryGroup -IncludeCloudBasedSources $true -PreferCloudBasedSources $true
```

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

### Add-CMManagementPoint

For more information, see [Add-CMManagementPoint](/powershell/module/configurationmanager/Add-CMManagementPoint).

**Non-breaking changes**

- When you use this cmdlet to enable communication with the cloud management gateway, it now by default configures the management point to support both internet and intranet clients.
- When you enable cloud gateway, **ClientConnectionTypes.InternetAndIntranet** is now the default value.

### Add-CMReportingServicePoint

For more information, see [Add-CMReportingServicePoint](/powershell/module/configurationmanager/Add-CMReportingServicePoint).

**Non-breaking changes**

This cmdlet will be blocked to run on PowerShell7, as SOAP is not supported in PowerShell7. This cmdlet requires the .NET Framework instead of .NET Core that's used with PowerShell version 7.

### Get-CMObjectSecurityScope

For more information, see [Get-CMObjectSecurityScope](/powershell/module/configurationmanager/Get-CMObjectSecurityScope).

**Non-breaking changes**

You can now use this cmdlet to get the security scope of a specified folder object.

### New-CMCloudManagementGateway

For more information, see [New-CMCloudManagementGateway](/powershell/module/configurationmanager/New-CMCloudManagementGateway).

**Non-breaking changes**

Added parameters **VMSSVMSize** and **Version** to support creating a cloud management gateway (CMG) using a virtual machine scale set.

### New-CMCoManagementPolicy

For more information, see [New-CMCoManagementPolicy](/powershell/module/configurationmanager/New-CMCoManagementPolicy).

**Non-breaking changes**

- You can now view the policy created as well as prevent creation of second policy from this cmdlet.
- You can now also create child policies for each workload, like UI, while creating Co-Management policy from this cmdlet.

### New-CMComplianceRuleRegistryKeyPermission

For more information, see [New-CMComplianceRuleRegistryKeyPermission](/powershell/module/configurationmanager/New-CMComplianceRuleRegistryKeyPermission).

**Bugs that were fixed**

Fixed an issue in **OperandDataType** property when creating a rule.

### Add-CMComplianceSettingWqlQuery

For more information, see [Add-CMComplianceSettingWqlQuery](/powershell/module/configurationmanager/Add-CMComplianceSettingWqlQuery).

**Non-breaking changes**

When using this cmdlet, you can now specify $null value to the parameter **WhereClause**.

### Set-CMClientSettingComplianceSetting

For more information, see [Set-CMClientSettingComplianceSetting](/powershell/module/configurationmanager/Set-CMClientSettingComplianceSetting).

**Non-breaking changes**

Added a new parameter **ScriptExecutionTimeoutSecs** to extend the script execution timeout value.

### Set-CMClientSettingClientCache

For more information, see [Set-CMClientSettingClientCache](/powershell/module/configurationmanager/Set-CMClientSettingClientCache).

**Non-breaking changes**

Added a new parameter **MinCacheTombstoneContentMins** to support setting the minimum duration before the client can remove cached content.

### Set-CMClientSettingComputerRestart

For more information, see [Set-CMClientSettingComputerRestart](/powershell/module/configurationmanager/Set-CMClientSettingComputerRestart).

**Non-breaking changes and bug fixes**

- Extended the validation range of the parameters **CountdownMins** and **RebootLogoffNotificationCountdownMins** to align with the console.
- Added new parameters **CountdownIntervalMins** and **ServerRebootLowRight** to align with the console.
- Fixed a property name issue for the parameter **NoRebootEnforcement**.

### Set-CMClientSettingEndpointProtection

For more information, see [Set-CMClientSettingEndpointProtection](/powershell/module/configurationmanager/Set-CMClientSettingEndpointProtection).

**Non-breaking changes**

You can now specify the defender agent type with the new parameter **DefenderAgent**.

### Get-CMNotification

For more information, see [Get-CMNotification](/powershell/module/configurationmanager/Get-CMNotification).

**Non-breaking changes**

- You can now use this cmdlet to get built-in notification by using parameter **IsBuiltIn**.
- You can now also use this cmdlet to get notification that could be dismissed by using parameter **CanDismiss**.
- New alias **InputObject** has been added for parameter **NotificationTasks** which now supports pipeline.

### New-CMFolder

For more information, see [New-CMFolder](/powershell/module/configurationmanager/New-CMFolder).

**Bugs that were fixed**

An issue in folder path validation has been fixed when using this cmdlet to create a new folder in the console.

## Changes to multiple cmdlets

The following folder-related cmdlets now support software update groups and automatic deployment rules:

- [Get-CMFolder](/powershell/module/configurationmanager/Get-CMFolder)
- [New-CMFolder](/powershell/module/configurationmanager/New-CMFolder)
- [Remove-CMFolder](/powershell/module/configurationmanager/Remove-CMFolder)
- [Set-CMFolder](/powershell/module/configurationmanager/Set-CMFolder)
- [Move-CMObject](/powershell/module/configurationmanager/Move-CMObject)
- [Add-CMObjectSecurityScope](/powershell/module/configurationmanager/Add-CMObjectSecurityScope)
- [Remove-CMObjectSecurityScope](/powershell/module/configurationmanager/Remove-CMObjectSecurityScope)

<!-- For more general information, see [Added folder support for nodes in the Software Library](/mem/configmgr/core/get-started/2022/technical-preview-2202#bkmk_folder). -->

The following cmdlets now have added validation condition for starting or stopping service while CMG is a Virtual Machine Scale Set:

- [Start-CMCloudManagementGateway](/powershell/module/configurationmanager/Start-CMCloudManagementGateway)
- [Stop-CMCloudManagementGateway](/powershell/module/configurationmanager/Stop-CMCloudManagementGateway)

The following cmdlets have been removed due to the deprecated RA feature: 

- [Add-CMCertificateRegistrationPoint](/powershell/module/configurationmanager/Add-CMCertificateRegistrationPoint)
- [Import-CMClientCertificatePfx](/powershell/module/configurationmanager/Import-CMClientCertificatePfx)
- [Import-CMWirelessProfileConfigurationItem](/powershell/module/configurationmanager/Import-CMWirelessProfileConfigurationItem)
- [New-CMCertificateProfilePfx](/powershell/module/configurationmanager/New-CMCertificateProfilePfx)
- [New-CMCertificateProfileScep](/powershell/module/configurationmanager/New-CMCertificateProfileScep)
- [New-CMCertificateProfileTrustedRootCA](/powershell/module/configurationmanager/New-CMCertificateProfileTrustedRootCA)
- [New-CMClientCertificateProfileConfigurationItem](/powershell/module/configurationmanager/New-CMClientCertificateProfileConfigurationItem)
- [New-CMEmailProfile](/powershell/module/configurationmanager/New-CMEmailProfile)
- [New-CMRootCertificateProfileConfigurationItem](/powershell/module/configurationmanager/New-CMRootCertificateProfileConfigurationItem)
- [New-CMVpnProfileConfigurationItem](/sccm-ps/ConfigurationManager/New-CMVpnProfileConfigurationItem)
- [New-CMWirelessProfile](/powershell/module/configurationmanager/New-CMWirelessProfile)
- [New-CMWirelessProfileConfigurationItem](/powershell/module/configurationmanager/New-CMWirelessProfileConfigurationItem)
- [Set-CMCertificateProfilePfx](/powershell/module/configurationmanager/Set-CMCertificateProfilePfx)
- [Set-CMCertificateProfileScep](/powershell/module/configurationmanager//Set-CMCertificateProfileScep)
- [Set-CMCertificateProfileTrustedRootCA](/powershell/module/configurationmanager/Set-CMCertificateProfileTrustedRootCA)
- [Set-CMCertificateRegistrationPoint](/powershell/module/configurationmanager/Set-CMCertificateRegistrationPoint)
- [Set-CMClientCertificateProfileConfigurationItem](/powershell/module/configurationmanager/Set-CMClientCertificateProfileConfigurationItem)
- [Set-CMEmailProfile](/powershell/module/configurationmanager/Set-CMEmailProfile)
- [Set-CMVpnProfileConfigurationItem](/powershell/module/configurationmanager/Set-CMVpnProfileConfigurationItem)
- [Set-CMWirelessProfile](/powershell/module/configurationmanager/Set-CMWirelessProfile)
- [Set-CMWirelessProfileConfigurationItem](/powershell/module/configurationmanager/Set-CMWirelessProfileConfigurationItem)

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To send feedback, use the Configuration Manager console. For more information, see [Feedback for PowerShell](/mem/configmgr/core/understand/product-feedback#feedback-for-powershell).
