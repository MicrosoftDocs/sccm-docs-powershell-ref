---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-CMComplianceRuleFileFolderDate

## SYNOPSIS
Sets a compliance rule file folder date

## SYNTAX

### ByCICreation (Default)
```
Set-CMComplianceRuleFileFolderDate [-Creation] -InputObject <IResultObject> -RuleName <String>
 [-ExpectedValue <DateTime[]>] [-ExpressionOperator <RuleExpressionOperator>] [-ReportNoncompliance <Boolean>]
 [-NewRuleName <String>] [-PassThru] [-Remediate <Boolean>] [-NoncomplianceSeverity <NoncomplianceSeverity>]
 [-RuleDescription <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByRuleCreation
```
Set-CMComplianceRuleFileFolderDate [-Creation] -Rule <Rule> [-ExpectedValue <DateTime[]>]
 [-ExpressionOperator <RuleExpressionOperator>] [-ReportNoncompliance <Boolean>] [-NewRuleName <String>]
 [-PassThru] [-Remediate <Boolean>] [-NoncomplianceSeverity <NoncomplianceSeverity>]
 [-RuleDescription <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByCIModified
```
Set-CMComplianceRuleFileFolderDate -InputObject <IResultObject> -RuleName <String>
 [-ExpectedValue <DateTime[]>] [-ExpressionOperator <RuleExpressionOperator>] [-Modification]
 [-ReportNoncompliance <Boolean>] [-NewRuleName <String>] [-PassThru] [-Remediate <Boolean>]
 [-NoncomplianceSeverity <NoncomplianceSeverity>] [-RuleDescription <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRuleModified
```
Set-CMComplianceRuleFileFolderDate -Rule <Rule> [-ExpectedValue <DateTime[]>]
 [-ExpressionOperator <RuleExpressionOperator>] [-Modification] [-ReportNoncompliance <Boolean>]
 [-NewRuleName <String>] [-PassThru] [-Remediate <Boolean>] [-NoncomplianceSeverity <NoncomplianceSeverity>]
 [-RuleDescription <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

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

### -Creation
{{Fill Creation Description}}

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
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
{{Fill ExpectedValue Description}}

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
{{Fill ExpressionOperator Description}}

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
{{Fill InputObject Description}}

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
{{Fill Modification Description}}

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
{{Fill NewRuleName Description}}

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
{{Fill NoncomplianceSeverity Description}}

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
{{Fill Remediate Description}}

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
{{Fill ReportNoncompliance Description}}

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
{{Fill Rule Description}}

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
{{Fill RuleDescription Description}}

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
{{Fill RuleName Description}}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
Microsoft.SystemsManagementServer.DesiredConfigurationManagement.Rules.Rule

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

