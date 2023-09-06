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

<!-- ## New cmdlets -->

<!-- - [<cmdlet>](/powershell/module/configurationmanager/): -->

## Cmdlet changes
The following changes have been made to existing cmdlets in this version. Changes may be new functionality or bug fixes. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.
<!-- CM Distrbution point cmdlets -->
### Add-CMDistributionPoint
For more information, see [Add-CMDistributionPoint](/powershell/module/configurationmanager/add-cmdistributionpoint).

**Non-breaking changes**

Two new parameters have been added to the cmdlet
 - _InitialMPForLookup:_ It is required (and requires) when providing -PreferredMPEnabled parameter. It expects a string input that represents the different lookup MP's separated by the '*' symbol. MP's are filtered based on the Site code of the DP, if the MP's site code is different, an error is thrown.
 - _PreferredMPEnabled:_ It is a switch parameter. The presence of the parameter indicates that the dynamic MP usage is enabled. PXE has to be enabled on the Distribution Point before using this parameter.

### Set-CMDistributionPoint
For more information, see [Set-CMDistributionPoint](/powershell/module/configurationmanager/set-cmdistributionpoint).

**Non-breaking changes**

Two new parameters have been added to the cmdlet
- _InitialMPForLookup:_ This parameter expects a string that represents the different lookup MP's separated by the symbol'*'. MP's are filtered out based on the Site code of the DP, if the MP's site code is different, an error is thrown.
- _PreferredMPEnabled:_ This is a boolean parameter where the $true value for the parameter indicates that the dynamic MP usage is enabled. PXE has to be enabled on the Distribution Point before using this parameter.

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
