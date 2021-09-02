---
description: Create a compliance rule for a simple file folder.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: New-CMComplianceRuleFileFolderSimple
---

# New-CMComplianceRuleFileFolderSimple

## SYNOPSIS

Create a compliance rule for a simple file folder.

## SYNTAX

```
New-CMComplianceRuleFileFolderSimple -PropertyType <SimpleFileFolderProperty>
 -ExpressionOperator <RuleExpressionOperator> [-ReportNoncompliance] -InputObject <ConfigurationItemSetting>
 -RuleName <String> [-ExpectedValue <String[]>] [-NoncomplianceSeverity <NoncomplianceSeverity>]
 [-RuleDescription <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a compliance rule for a simple file folder.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
$ci = Get-CMConfigurationItem -Name "ci1" -Fast

$Result = $ci | Add-CMComplianceSettingFile -Path "C:\" -FileName  "TestFile.exe" -NoRule -Name "AttributeSetting1"

$TestSet = $Result | Get-CMComplianceSetting -SettingName "AttributeSetting1"

$r1 = $TestSet | New-CMComplianceRuleFileFolderSimple -PropertyType SHA1Hash -RuleName "RuleSha1HashEquals" -ExpressionOperator IsEquals -ExpectedValue "s4XuFV2KZldXAMQZ6YEWFv+5zA6ZB982Fbh471TMboc="

$r2 = $TestSet | New-CMComplianceRuleFileFolderSimple -PropertyType Company -RuleName "RuleCompanyEquals" -ExpressionOperator IsEquals -ExpectedValue "Contoso"

$r3 = $TestSet | New-CMComplianceRuleFileFolderSimple -PropertyType ProductName -RuleName "RuleProductNameEquals" -ExpressionOperator IsEquals -ExpectedValue "MyContoso"

$Result | Add-CMComplianceSettingRule -Rule $r1

$Result | Add-CMComplianceSettingRule -Rule $r2

$Result | Add-CMComplianceSettingRule -Rule $r3
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

### -ExpectedValue

Specify an array of strings to compare the value. The value to compare depends upon the specified **PropertyType**.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ExpectedValues

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator

For the **ExpectedValue**, specify the comparison operator.

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

Specify a configuration item setting object as the target of this rule.

```yaml
Type: ConfigurationItemSetting
Parameter Sets: (All)
Aliases: Setting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoncomplianceSeverity

Specify the severity level for reports when the rule is noncompliant.

```yaml
Type: NoncomplianceSeverity
Parameter Sets: (All)
Aliases:
Accepted values: None, Informational, Warning, Critical, CriticalWithEvent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyType

Specify the folder property to compare and assess for compliance. Use the **-ExpectedValue** parameter to specify the value of this property, and the **-ExpressionOperator** parameter to specify the means of comparison.

Starting in version 2010, the parameter type changed from _FileFolderProperty_ to _SimpleFileFolderProperty_ type.

```yaml
Type: SimpleFileFolderProperty
Parameter Sets: (All)
Aliases:
Accepted values: Company, ProductName, SHA1Hash

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportNoncompliance

Add this parameter to report noncompliance if this setting instance isn't found.

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

### -RuleDescription

Specify an optional description for this rule.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleName

Specify the name for this rule.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.DesiredConfigurationManagement.ConfigurationItemSetting
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Add-CMComplianceSettingFile](Add-CMComplianceSettingFile.md)

[Get-CMComplianceSetting](Get-CMComplianceSetting.md)

[Add-CMComplianceSettingRule](Add-CMComplianceSettingRule.md)
