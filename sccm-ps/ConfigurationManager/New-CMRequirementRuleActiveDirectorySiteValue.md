---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
online version:
schema: 2.0.0
---

# New-CMRequirementRuleActiveDirectorySiteValue

## SYNOPSIS

Create an Active Directory site value requirement rule for an application deployment type.

## SYNTAX

```
New-CMRequirementRuleActiveDirectorySiteValue -RuleOperator <RuleExpressionOperator> -Site <String[]>
 [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an Active Directory site value requirement rule for an application deployment type.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this requirement rule object to either the **AddRequirement** or **RemoveRequirement** parameters.

For more information, see [Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require) and [Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a requirement rule for Active Directory sites

This example first uses the **Get-CMGlobalCondition** cmdlet to get the default **Active Directory site** global condition. It then defines a string array of two Active Directory sites. Next it creates the requirement rule object. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

```powershell
$gc = Get-CMGlobalCondition -Name "Active Directory site"
$sites = @('London', 'Wells')
$rule = New-CMRequirementRuleActiveDirectorySiteValue -InputObject $gc -RuleOperator OneOf -Site $sites

Set-CMScriptDeploymentType -ApplicationName "Central App" -DeploymentTypeName "Install" -AddRequirement $rule
```

## PARAMETERS

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

In most instances, you'll use the default **Active Directory site** global condition, for example: `Get-CMGlobalCondition -Name "Active Directory site"`.

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

### -Site

Specify a string array of Active Directory site names.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Sites, SiteName, SiteNames

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
[New-CMRequirementRuleOperatingSystemLanguageValue](New-CMRequirementRuleOperatingSystemLanguageValue.md)
[New-CMRequirementRuleOperatingSystemValue](New-CMRequirementRuleOperatingSystemValue.md)
[New-CMRequirementRuleOUValue](New-CMRequirementRuleOUValue.md)
[New-CMRequirementRuleRegistryKeyPermissionValue](New-CMRequirementRuleRegistryKeyPermissionValue.md)
[New-CMRequirementRuleScreenResolutionValue](New-CMRequirementRuleScreenResolutionValue.md)
[Get-CMGlobalCondition](Get-CMGlobalCondition.md)
[Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require)
[Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions)
