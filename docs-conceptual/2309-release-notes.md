---
title: Version 2309 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2309.
ms.date: 09/13/2023
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
ms.localizationpriority: null
author: banreet
ms.author: banreetkaur
manager: sunitashaw
---

# Configuration Manager cmdlet library changes for version 2309

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2309.

> [!NOTE]
> Configuration Manager current branch version 2111 is the baseline for these changes. For more information, see [Configuration Manager cmdlet library changes for version 2111](2111-release-notes.md).

<!--
## Module changes
 -->

## New cmdlets 

<!-- - [<cmdlet>](/powershell/module/configurationmanager/): -->
### New-CMWindows11EditionUpgrade

Use this cmdlet to create a Windows 11 edition upgrade policy. For more information, see [About upgrading windows version in Configuration Manager](/mem/configmgr/compliance/deploy-use/upgrade-windows-version).

```powershell
New-CMWindows11EditionUpgrade -Name "NewEditionPolicyByKey" -WindowsEdition Windows11Enterprise -ProductKey "123ab-cd456-789ef-2j3k4-0ghi1"
```
### Set-UpdateServerApplication
Use this cmdlet to add the missing URL 'http://localhost' to your existing server app. For more information, see [About creating and deploying applications in Configuration Manager](/mem/configmgr/apps/get-started/create-and-deploy-an-application).

```powershell
SET-UpdateServerApplication -TenantId 1E7C0B63-1DAB-4754-8433-AF8F9CFFCF38
```

## Cmdlet changes
The following changes have been made to existing cmdlets in this version. Changes may be new functionality or bug fixes. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.
<!-- CM Distrbution point cmdlets -->
### Add-CMDistributionPoint
For more information, see [Add-CMDistributionPoint](/powershell/module/configurationmanager/add-cmdistributionpoint).

**Non-breaking changes**

Two new parameters have been added to the cmdlet
 - _InitialMPForLookup:_ It's required (and requires) when providing -PreferredMPEnabled parameter. It expects a string input that represents the different lookup MP's separated by the * symbol. MP's are filtered based on the Site code of the DP, if the MP's site code is different, an error is thrown.
 - _PreferredMPEnabled:_ It's a switch parameter. The presence of the parameter indicates that the dynamic MP usage is enabled. PXE has to be enabled on the Distribution Point before using this parameter.

### Set-CMDistributionPoint
For more information, see [Set-CMDistributionPoint](/powershell/module/configurationmanager/set-cmdistributionpoint).

**Non-breaking changes**

Two new parameters have been added to the cmdlet
- _InitialMPForLookup:_ This parameter expects a string that represents the different lookup MP's separated by the symbol'*'. MP's are filtered out based on the Site code of the DP, if the MP's site code is different, an error is thrown.
- _PreferredMPEnabled:_ This parameter is boolean where the $true value for the parameter indicates that the dynamic MP usage is enabled. PXE has to be enabled on the Distribution Point before using this parameter.

### Invoke-CMScript
For more information, see [Invoke-CMScript](/powershell/module/configurationmanager/invoke-cmscript).

**Non-breaking changes**

A new optional parameter, ScheduleTime, has been added to the Invoke-CMScript cmdlet. It specifies the script runtime(UTC).
```powershell
$ScriptObj = Get-CMScript -ScriptName "test"
Invoke-CMScript -InputObject $ScriptObj -CollectionId "SMSDM003" -ScheduleTime "08/02/2023 07:35:00"
```
### New-CMCloudManagementGateway
For more information, see [New-CMCloudManagementGateway](/powershell/module/configurationmanager/new-cmcloudmanagementgateway).

**Non-breaking changes**

A new parameter, TenantId, has been added to the New-CMCloudManagementGateway cmdlet.  

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To send feedback, use the Configuration Manager console. For more information, see [Feedback for PowerShell](/mem/configmgr/core/understand/product-feedback#feedback-for-powershell).
