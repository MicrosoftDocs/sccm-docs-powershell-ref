---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/04/2021
online version:
schema: 2.0.0
---

# New-CMRequirementRuleOperatingSystemLanguageValue

## SYNOPSIS

Create an OS language requirement rule for an application deployment type.

## SYNTAX

```
New-CMRequirementRuleOperatingSystemLanguageValue -Culture <CultureInfo[]> [-IsMobile <Boolean>]
 -RuleOperator <RuleExpressionOperator> [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an OS language requirement rule for an application deployment type.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this requirement rule object to either the **AddRequirement** or **RemoveRequirement** parameters.

For more information, see [Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require) and [Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a requirement rule for an OS language

This example first uses the **Get-CMGlobalCondition** cmdlet to get the default **OS language** global condition for non-mobile Windows devices. It then defines variables for two locales, **Irish (Ireland)** (`ga-IE`) and **Hungarian (Hungary)** (`hu-HU`). Next it creates the requirement rule object to include these two locales. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

```powershell
$myGC = Get-CMGlobalCondition -Name "Operating System Language" | Where-Object PlatformType -eq 1

$cultureA = [System.Globalization.CultureInfo]::GetCultures([System.Globalization.CultureTypes]::AllCultures) | Where-Object Name -eq "ga-IE"

$cultureB = [System.Globalization.CultureInfo]::GetCultures([System.Globalization.CultureTypes]::AllCultures) | Where-Object Name -eq "hu-HU"

$myRule = $myGC | New-CMRequirementRuleOperatingSystemLanguageValue -RuleOperator OneOf -Culture $cultureA,$cultureB -IsMobile $False

Set-CMScriptDeploymentType -ApplicationName "Central App" -DeploymentTypeName "Install" -AddRequirement $myRule
```

## PARAMETERS

### -Culture

Specify one or more culture objects. Use the following syntax to specify a culture object:

`[System.Globalization.CultureInfo]::GetCultures([System.Globalization.CultureTypes]::AllCultures)`

By default, Windows has over 800 cultures built-in. To filter the results, pass the results of the above command through the pipeline to the **Where-Object** cmdlet. Filter on one of the following properties:

- **LCID**: The language code identifier. For example, English (United States) is `1033`.
- **Name**: The language code name. For example, English (United States) is `en-US`.
- **Display name**: The language display name. For example, `English (United States)`.

For more information and a list of cultures, see [Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

```yaml
Type: CultureInfo[]
Parameter Sets: (All)
Aliases: Cultures

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a global condition object to use as the basis for this requirement rule. To get this object, use the [Get-CMGlobalCondition](Get-CMGlobalCondition.md) cmdlet.

In most instances, you'll use the default **Operating system language** global condition for non-mobile Windows devices. For example: `Get-CMGlobalCondition -Name "Operating System Language" | Where-Object PlatformType -eq 1`.

> [!NOTE]
> By default, Configuration Manager has two global conditions named **Operating system language**. You can distinguish them by device type using the **PlatformType** property:
>
> |PlatformType|Device type|
> |---------|---------|
> |`1`|Windows|
> |`2`|Mobile|

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: GlobalCondition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsMobile

If you use the mobile device type global condition, set this parameter to `$true`.

If you get the OS language global condition with `PlatformType -eq 1`, don't include this parameter or set it to `$false`.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleOperator

Specify the operator to compare the device's setting with the expected value.

```yaml
Type: RuleExpressionOperator
Parameter Sets: (All)
Aliases:
Accepted values: OneOf, NoneOf

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMRequirementRuleActiveDirectorySiteValue](New-CMRequirementRuleActiveDirectorySiteValue.md)
[New-CMRequirementRuleBooleanValue](New-CMRequirementRuleBooleanValue.md)
[New-CMRequirementRuleCMSiteValue](New-CMRequirementRuleCMSiteValue.md)
[New-CMRequirementRuleCommonValue](New-CMRequirementRuleCommonValue.md)
[New-CMRequirementRuleDeviceOwnershipValue](New-CMRequirementRuleDeviceOwnershipValue.md)
[New-CMRequirementRuleExistential](New-CMRequirementRuleExistential.md)
[New-CMRequirementRuleExpression](New-CMRequirementRuleExpression.md)
[New-CMRequirementRuleFileAttributeValue](New-CMRequirementRuleFileAttributeValue.md)
[New-CMRequirementRuleFilePermissionValue](New-CMRequirementRuleFilePermissionValue.md)
[New-CMRequirementRuleFreeDiskSpaceValue](New-CMRequirementRuleFreeDiskSpaceValue.md)
[New-CMRequirementRuleInputTypeValue](New-CMRequirementRuleInputTypeValue.md)
[New-CMRequirementRuleOperatingSystemValue](New-CMRequirementRuleOperatingSystemValue.md)
[New-CMRequirementRuleOUValue](New-CMRequirementRuleOUValue.md)
[New-CMRequirementRuleRegistryKeyPermissionValue](New-CMRequirementRuleRegistryKeyPermissionValue.md)
[New-CMRequirementRuleScreenResolutionValue](New-CMRequirementRuleScreenResolutionValue.md)
[Get-CMGlobalCondition](Get-CMGlobalCondition.md)
[Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require)
[Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions)
[Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c)
