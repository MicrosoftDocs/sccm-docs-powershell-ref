---
description: Sets a compliance rule file folder date.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMComplianceRuleFileFolderDate
---

# Set-CMComplianceRuleFileFolderDate

## SYNOPSIS
Sets a compliance rule file folder date.

## SYNTAX

### ByCICreation (Default)
```
Set-CMComplianceRuleFileFolderDate [-Creation] [-ExpectedValue <DateTime[]>]
 [-ExpressionOperator <RuleExpressionOperator>] -InputObject <IResultObject> -RuleName <String>
 [-ReportNoncompliance <Boolean>] [-NewRuleName <String>] [-PassThru] [-Remediate <Boolean>]
 [-NoncomplianceSeverity <NoncomplianceSeverity>] [-RuleDescription <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRuleCreation
```
Set-CMComplianceRuleFileFolderDate [-Creation] [-ExpectedValue <DateTime[]>]
 [-ExpressionOperator <RuleExpressionOperator>] -Rule <Rule> [-ReportNoncompliance <Boolean>]
 [-NewRuleName <String>] [-PassThru] [-Remediate <Boolean>] [-NoncomplianceSeverity <NoncomplianceSeverity>]
 [-RuleDescription <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByCIModified
```
Set-CMComplianceRuleFileFolderDate [-ExpectedValue <DateTime[]>] [-ExpressionOperator <RuleExpressionOperator>]
 -InputObject <IResultObject> [-Modification] -RuleName <String> [-ReportNoncompliance <Boolean>]
 [-NewRuleName <String>] [-PassThru] [-Remediate <Boolean>] [-NoncomplianceSeverity <NoncomplianceSeverity>]
 [-RuleDescription <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByRuleModified
```
Set-CMComplianceRuleFileFolderDate [-ExpectedValue <DateTime[]>] [-ExpressionOperator <RuleExpressionOperator>]
 [-Modification] -Rule <Rule> [-ReportNoncompliance <Boolean>] [-NewRuleName <String>] [-PassThru]
 [-Remediate <Boolean>] [-NoncomplianceSeverity <NoncomplianceSeverity>] [-RuleDescription <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -Creation
```yaml
Type: SwitchParameter
Parameter Sets: ByCICreation, ByRuleCreation
Aliases:

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

### -ExpectedValue
```yaml
Type: DateTime[]
Parameter Sets: (All)
Aliases: ExpectedValues, ExpectedDate, ExpectedDates

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator
```yaml
Type: RuleExpressionOperator
Parameter Sets: (All)
Aliases:
Accepted values: IsEquals, NotEquals, GreaterThan, LessThan, Between, GreaterEquals, LessEquals, OneOf, NoneOf

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
```yaml
Type: IResultObject
Parameter Sets: ByCICreation, ByCIModified
Aliases: ConfigurationItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Modification
```yaml
Type: SwitchParameter
Parameter Sets: ByCIModified, ByRuleModified
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewRuleName
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

### -NoncomplianceSeverity
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

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -Remediate
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

### -ReportNoncompliance
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

### -Rule
```yaml
Type: Rule
Parameter Sets: ByRuleCreation, ByRuleModified
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RuleDescription
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
```yaml
Type: String
Parameter Sets: ByCICreation, ByCIModified
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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
### Microsoft.SystemsManagementServer.DesiredConfigurationManagement.Rules.Rule
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
