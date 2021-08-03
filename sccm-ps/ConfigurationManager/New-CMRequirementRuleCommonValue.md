---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
online version:
schema: 2.0.0
---

# New-CMRequirementRuleCommonValue

## SYNOPSIS

Create a requirement rule to evaluate a value-based global condition on an application deployment type.

## SYNTAX

```
New-CMRequirementRuleCommonValue [-PropertyForAssembly <AssemblyProperty>]
 [-PropertyForFileFolder <FileFolderProperty>] -RuleOperator <RuleExpressionOperator> -Value1 <String[]>
 [-Value2 <String[]>] [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a requirement rule on an application deployment type that evaluates a global condition with a **Value** rule type.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this requirement rule object to either the **AddRequirement** or **RemoveRequirement** parameters.

For more information, see [Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require) and [Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a requirement rule for number of processors

This example first uses the **Get-CMGlobalCondition** cmdlet to get the default **Number of processors** global condition. Next it creates the requirement rule object to evaluate the global condition on the device to be greater than or equal to two. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

In other words, the device needs to have at least two processors for the app to install.

```powershell
$myGC = Get-CMGlobalCondition -Name "Number of processors"
$myRule = New-CMRequirementRuleCommonValue -GlobalCondition $myGC -Value1 "2" -RuleOperator GreaterEquals

Set-CMScriptDeploymentType -ApplicationName "Central app" -DeploymentTypeName "Install" -AddRequirement $myRule
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

The global condition needs to support the **Rule type** of **Value**.

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

### -PropertyForAssembly

If the global condition supports it, specify the assembly property to compare with the expected value.

```yaml
Type: AssemblyProperty
Parameter Sets: (All)
Aliases:
Accepted values: Culture, Version, PublicKeyToken

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyForFileFolder

If the global condition supports it, specify a file or folder property to compare with the expected value.

For example:

`$myRule = New-CMRequirementRuleCommonValue -GlobalCondition $myGC -PropertyForFileFolder DateCreated -Value1 "2018-08-07T05:32:45Z" -RuleOperator GreaterEquals`

```yaml
Type: FileFolderProperty
Parameter Sets: (All)
Aliases:
Accepted values: Size, Version, DateCreated, DateModified, Company, ProductName, SHA1Hash, Permissions, Attributes

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
Accepted values: And, Or, Other, IsEquals, NotEquals, GreaterThan, LessThan, Between, NotBetween, GreaterEquals, LessEquals, BeginsWith, NotBeginsWith, EndsWith, NotEndsWith, Contains, NotContains, AllOf, OneOf, NoneOf, SetEquals, SubsetOf, ExcludesAll

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value1

Specify a string or array of expected values to compare.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value2

If you use a **RuleOperator** like `Between`, use this parameter to specify the upper value.

For example:



$myRule = New-CMRequirementRuleCommonValue -GlobalCondition $GC -PropertyForFileFolder Size -Value1 200 -Value2 300 -RuleOperator Between

```yaml
Type: String[]
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMRequirementRuleActiveDirectorySiteValue](New-CMRequirementRuleActiveDirectorySiteValue.md)
[New-CMRequirementRuleBooleanValue](New-CMRequirementRuleBooleanValue.md)
[New-CMRequirementRuleCMSiteValue](New-CMRequirementRuleCMSiteValue.md)
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
