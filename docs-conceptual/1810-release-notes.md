---
title: Version 1810 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 1810. 
ms.date: 02/20/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Configuration Manager Cmdlet Library changes for version 1810

*Applies to: Configuration Manager (Current Branch)*

> [!NOTE]  
> Configuration Manager current branch version 1806 is the baseline for these changes. For more information, see [Configuration Manager Cmdlet Library changes for version 1806](https://docs.microsoft.com/powershell/sccm/1806_release_notes).

## Important changes

### New cmdlets
The following cmdlets are added to create requirement rules for deployment types and global conditions:
- New-CMGlobalConditionExpression
- New-CMRegistryAccessControlEntry
- New-CMRequirementRuleActiveDirectorySiteValue
- New-CMRequirementRuleBooleanValue
- New-CMRequirementRuleCMSiteValue
- New-CMRequirementRuleCommonValue
- New-CMRequirementRuleDeviceOwnershipValue
- New-CMRequirementRuleExistential
- New-CMRequirementruleExpression
- New-CMRequirementRuleFileAttributeValue
- New-CMRequirementRuleFilePermissionValue
- New-CMRequirementRuleFreeDiskSpaceValue
- New-CMRequirementRuleInputTypeValue
- New-CMRequirementRuleOperatingSystemLanguageValue
- New-CMRequirementRuleOperatingSystemValue
- New-CMRequirementRuleOUValue
- New-CMRequirementRuleScreenResolutionValue

Supported cmdlets for Add and Set-CM*DeploymentType have added parameters for **GroupDetectionClauses** and **DetectionClauseConnector**.

#### Examples

##### Create a simple expression with a rule
```powershell
$rule1 = Get-CMGlobalCondition -Name "Total physical memory" | New-CMRequirementRuleCommonValue -Value1 2048 -RuleOperator GreaterEquals
$myRuleExpression = New-CMRequirementRuleExpression -AddRequirementRule $rule1
$myGC = New-CMGlobalConditionExpression -Name "GCExp" -DeviceType Windows -RootExpression $myRuleExpression
```

##### Add a complex global condition expression
```powershell
$ruleProc = Get-CMGlobalCondition -Name "Number of processors" | New-CMRequirementRuleCommonValue -Value1 2 -RuleOperator GreaterEquals
$ruleMem1 = Get-CMGlobalCondition -Name "Total physical memory" | New-CMRequirementRuleCommonValue -Value1 2048 -RuleOperator GreaterThan
$ruleMem2 = Get-CMGlobalCondition -Name "Total physical memory" | New-CMRequirementRuleCommonValue -Value1 4096 -RuleOperator LessEquals
$ruleCPUSpeed1 = Get-CMGlobalCondition -Name "CPU Speed" | New-CMRequirementRuleCommonValue -Value1 5120 -RuleOperator LessEquals
$ruleCPUSpeed2 = Get-CMGlobalCondition -Name "CPU Speed" | New-CMRequirementRuleCommonValue -Value1 1024 -RuleOperator GreaterThan
$expressionProc = New-CMRequirementRuleExpression -AddRequirementRule $ruleProc
$expressionMem = New-CMRequirementRuleExpression -AddRequirementRule $ruleMem1, $ruleMem2 -ClauseOperator And
$expressionCPU = New-CMRequirementRuleExpression -AddRequirementRule $ruleCPUSpeed1, $ruleCPUSpeed2 -ClauseOperator And
$myRuleExpression = New-CMRequirementRuleExpression -RootExpression $expressionProc -AddExpression $expressionMem,$expressionCPU -ClauseOperator And -AddAsGroup -GroupOperator Or
$myGC = New-CMGlobalConditionExpression -Name "GCExp" -DeviceType Windows -RootExpression $myRuleExpression
```

##### Add a language rule
```powershell
$myGC = Get-CMGlobalCondition -Name "Operating System Language" | Where-Object PlatformType -eq 1
$cultureA = [System.Globalization.CultureInfo]::GetCultures([System.Globalization.CultureTypes]::AllCultures) | Where-Object Name -eq "zh"
$cultureB = [System.Globalization.CultureInfo]::GetCultures([System.Globalization.CultureTypes]::AllCultures) | Where-Object Name -eq "zh-CN"
$myRule = $myGC | New-CMRequirementRuleOperatingSystemLanguageValue -RuleOperator NoneOf -Culture $cultureA,$cultureB -IsMobile $False
Set-CMScriptDeploymentType -ApplicationName "myApp" -DeploymentTypeName "myDT" -AddRequirement $myRule
```

##### Create a simple expression with a rule.
```powershell
$clauseFile1 = New-CMDetectionClauseFile -FileName "abc" -Path "c:\abc" -PropertyType Size -ExpectedValue 1024 -ExpressionOperator IsEquals -Value
$clauseFile2 = New-CMDetectionClauseFile -FileName "abc" -Path "c:\abc" -PropertyType Size -ExpectedValue 2048 -ExpressionOperator IsEquals -Value
$clauseFile3 = New-CMDetectionClauseFile -FileName "abc" -Path "c:\abc" -PropertyType Size -ExpectedValue 4096 -ExpressionOperator IsEquals -Value

Set-CMScriptDeploymentType -ApplicationName "testApp1" -DeploymentTypeName "abc" -AddDetectionClause $clauseFile1,$clauseFile2,$clauseFile3 -DetectionClauseConnector @{"LogicalName"=$clauseFile3.Setting.LogicalName;"Connector"="OR"} -GroupDetectionClauses $clauseFile2.Setting.LogicalName, $clauseFile3.Setting.LogicalName
```

### Removed cmdlets
None

### Deprecated cmdlets
None



## Known issues

The following items are known issues with the Cmdlet Library that aren't resolved in this version.


### Get-CMAadConditionalAccessPolicy and Set-CMAadConditionalAccessPolicy

These cmdlets require a 64-bit PowerShell environment.

#### Workaround
- None


### Import-CMSecurityRole

Cmdlet may fail with a DirectoryNotFoundException error locating the file `SecuredRoles.xsd`.

#### Workaround
- Call `Import-Module` against the `ConfigurationManager.psd1` file, and not the logical path or module name.


### Set-CMSoftwareUpdatePoint

Changes to **Schedule** may not be shown in the Configuration Manager console even though the underlying SMS Provider object has been changed.

#### Workaround
- Quit and relaunch the Configuration Manager console.


### Resource tracking and recovery (beta)

This version adds new cmdlets to support tracking SMS Provider objects used by the PowerShell runtime, and to clean up these resources when they're no longer needed.

- Disconnect-CMObject
- Start-CMObjectTracking
- Stop-CMObjectTracking

When you run `Start-CMObjectTracking`, the PowerShell runtime tracks `IResultObject` objects created by Cmdlet Library cmdlets. For cmdlets that aren't manually cleaned up with `.Dispose()`, reclaim them by using `Disconnect-CMObject` against an individual object.

#### Example
```powershell
# Reclaim a single tracked object
$o | Disconnect-CMObject

# Reclaim all tracked objects
Disconnect-CMObject -All
```

Once an object is reclaimed, it can no longer be reused or passed to another cmdlet through the object pipeline.

`Stop-CMObjectTracking` can be used to turn off object tracking. Previously allocated objects remain active.

Unclaimed resources can cause the SMS Provider to raise quota violation errors. These quota issues typically manifest from working with large sets of SMS Provider objects or in long-running environments.

> [!NOTE]  
> This feature is experimental and may be subject to change or removal in a future release. It's opt-in and isn't enabled by default.  



## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

### Add-CMDistributionPoint
#### Non-breaking changes
- New **EnableLedbat** parameter to enable LEDBAT for a distribution point

### Add-CMIntuneSubscription
#### Bugs that were fixed
- Can't set **CompanyLogoPath** or **CompanyLogoThemedPath** to artwork larger than 400x100 and 750 KB

### Add-CMManagementPoint
#### Bugs that were fixed
- If **EnableCloudGateway** is `$true`, can set **CommunicationType** to unsupported value of `Http` 

### Clear-CMPxeDeployment
#### Bugs that were fixed
- Cmdlet doesn't clear PXE deployments

### Get-CMDevice
#### Bugs that were fixed
- Cmdlet may not return expected properties for a device

### Get-CMHierarchySetting
#### Non-breaking changes
- Cmdlet now returns client upgrade and usage data settings

### New-CMAntimalwarePolicyDeployment
#### Bugs that were fixed
- Cmdlet allows a user collection to be specified as a deployment target

### New-CMComplianceRuleExistential
#### Non-breaking changes
- **ExpectedValue** parameter now allows for negative numbers

### New-CMConfigurationPolicyuDeployment
#### Bugs that were fixed
- **PostponeDateTime** parameter not available in all parameter sets

### New-CMUserDataAndProfileConfigurationItem
#### Bugs that were fixed
- Can't use `$false` with **DetectSlowLinkDisabled** parameter
- Some parameters can't be set when **DetectSlowLink** is `$true`

### New-CMWirelessProfile
#### Non-breaking changes
- Can now use 'Fast' with **EapType** parameter
- New **RememberUserCredentials** parameter can be used to set or clear credentials.
#### Deprecations
- **RememberCredentials** parameter has been superseded by **RememberUserCredentials**

### Set-CMComplianceRuleExistential
#### Non-breaking changes
- **ExpectedValue** parameter now allows for negative numbers

### Set-CMDistributionPoint
#### Non-breaking changes
- New **EnableLedbat** parameter to configure LEDBAT for a distribution point

### Set-CMHierarchySetting
#### Non-breaking changes
- New **TelemetryLevel** parameter for configuring usage data settings

### Set-CMIntuneSubscription
#### Bugs that were fixed
- Can't set **CompanyLogoPath** or **CompanyLogoThemedPath** to artwork larger than 400x100 and 750KB

### Set-CMManagementPoint
#### Bugs that were fixed
- If **EnableCloudGateway** is `$true`, can set **CommunicationType** to unsupported value of `Http`

### Set-CMMsiDeploymentType
#### Bugs that were fixed
- **AddDetectionClause** parameter clears previously existing MSI product code detection clause
- **AddRequirement** parameter may fail with "SQL_ERROR"
#### Non-breaking changes
- New **GroupDetectionClauses** and **DetectionClauseConnector** parameters for grouping detection clauses

### Set-CMSoftwareUpdatePointComponent
#### Non-breaking changes
- Added new parameters to configure feature and non-feature supersedence
- New **ImmediatelyExpireSupersedenceForFeature** parameter to immediately expire superseded updates
- New **WaitForMonthFeature** parameter to configure how long to expire superseded updates

### Set-CMTSStepJoinDomainWorkgroup
#### Bugs that were fixed
- **UserName** parameter doesn't support `%VARIABLE%` format

### Set-CMTSStepCaptureUserState
#### Non-breaking changes
- Cmdlet now warns when **AddConfigFile** is used and **ModeOption** is `Standard`

### Set-CMUserDataAndProfileConfigurationItem
#### Non-breaking changes
- Cmdlet now warns when **SlowLink** and **SyncMins** parameter are used when **EnableSlowLink** is `$false`

### Set-CMWirelessProfile
#### Non-breaking changes
- Can now use 'Fast' with **EapType** parameter
- New **RememberUserCredentials** parameter can be used to set or clear credentials.
#### Deprecations
- **RememberCredentials** parameter has been superseded by **RememberUserCredentials**

### Start-CMAntimalwarePolicyDeployment
#### Bugs that were fixed
- Cmdlet allows a user collection to be specified as a deployment target



## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To submit bug reports, use [send a smile in the Configuration Manager console](https://docs.microsoft.com/sccm/core/understand/find-help#product-feedback). For new feature requests, use [UserVoice](https://configurationmanager.uservoice.com).



