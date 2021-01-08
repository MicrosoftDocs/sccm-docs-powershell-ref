---
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
online version:
schema: 2.0.0
---

# New-CMRequirementRuleExpression

## SYNOPSIS

Create a requirement rule to evaluate a custom global condition with a complex expression.

## SYNTAX

```
New-CMRequirementRuleExpression [-AddAsGroup] [-AddExpression <ExpressionBase[]>]
 [-AddRequirementRule <Rule[]>] [-ClauseOperator <ConnectOperator>] [-GroupOperator <ConnectOperator>]
 [-RootExpression <ExpressionBase>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a requirement rule on an application deployment type that evaluates a custom global condition with a complex expression. When you create a global condition, the **Condition type** needs to be **Expression**. These expressions let you add multiple clauses and group them with logical operators.

To create a custom global condition with an expression, use the [New-CMGlobalConditionExpression](New-CMGlobalConditionExpression.md) cmdlet.

After you use the **New-CMRequirementRuleExpression** cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this requirement rule object to either the **AddRequirement** or **RemoveRequirement** parameters.

For more information, see [Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require) and [Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a basic expression

```powershell
$rule1 = Get-CMGlobalCondition -Name "Total physical memory" | New-CMRequirementRuleCommonValue -Value1 2048 -RuleOperator GreaterEquals
$myRuleExpression = New-CMRequirementRuleExpression -AddRequirementRule $rule1
$myGC = New-CMGlobalConditionExpression -Name "GCExp" -DeviceType Windows -RootExpression $myRuleExpression
```

### Example 2: Add a complex global condition expression

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

## PARAMETERS

### -AddAsGroup

Add this parameter to add the expressions as a group. Specify more than one expression with the **AddExpression** parameter. Use the **GroupOperator** parameter to specify the connector.

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

### -AddExpression

Specify one or more expression objects to add to a new expression. Create these objects with this same cmdlet. Use the **RootExpression** parameter to specify the first expression.

```yaml
Type: ExpressionBase[]
Parameter Sets: (All)
Aliases: AddExpressions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRequirementRule

Specify an array of requirement objects for the expression. To create a requirement rule object, use one of the following cmdlets:

- [New-CMRequirementRuleActiveDirectorySiteValue](New-CMRequirementRuleActiveDirectorySiteValue.md)
- [New-CMRequirementRuleBooleanValue](New-CMRequirementRuleBooleanValue.md)
- [New-CMRequirementRuleCMSiteValue](New-CMRequirementRuleCMSiteValue.md)
- [New-CMRequirementRuleCommonValue](New-CMRequirementRuleCommonValue.md)
- [New-CMRequirementRuleDeviceOwnershipValue](New-CMRequirementRuleDeviceOwnershipValue.md)
- [New-CMRequirementRuleExistential](New-CMRequirementRuleExistential.md)
- [New-CMRequirementRuleExpression](New-CMRequirementRuleExpression.md)
- [New-CMRequirementRuleFileAttributeValue](New-CMRequirementRuleFileAttributeValue.md)
- [New-CMRequirementRuleFilePermissionValue](New-CMRequirementRuleFilePermissionValue.md)
- [New-CMRequirementRuleFreeDiskSpaceValue](New-CMRequirementRuleFreeDiskSpaceValue.md)
- [New-CMRequirementRuleInputTypeValue](New-CMRequirementRuleInputTypeValue.md)
- [New-CMRequirementRuleOperatingSystemLanguageValue](New-CMRequirementRuleOperatingSystemLanguageValue.md)
- [New-CMRequirementRuleOperatingSystemValue](New-CMRequirementRuleOperatingSystemValue.md)
- [New-CMRequirementRuleOUValue](New-CMRequirementRuleOUValue.md)
- [New-CMRequirementRuleRegistryKeyPermissionValue](New-CMRequirementRuleRegistryKeyPermissionValue.md)
- [New-CMRequirementRuleScreenResolutionValue](New-CMRequirementRuleScreenResolutionValue.md)

```yaml
Type: Rule[]
Parameter Sets: (All)
Aliases: AddRequirementRules

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClauseOperator

Specify the logical operator to use as the connector between multiple expressions.

```yaml
Type: ConnectOperator
Parameter Sets: (All)
Aliases:
Accepted values: And, Or

Required: False
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

### -GroupOperator

Specify the logical operator to use as the connector between groups. Use this parameter with the **AddAsGroup** parameter.

```yaml
Type: ConnectOperator
Parameter Sets: (All)
Aliases:
Accepted values: And, Or

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RootExpression

Specify the first expression with this parameter. Create an expression object with this same cmdlet. To add more than one expression, also use the **AddExpression** parameter.

```yaml
Type: ExpressionBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

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
[New-CMGlobalConditionExpression](New-CMGlobalConditionExpression.md)
[Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require)
[Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions)
