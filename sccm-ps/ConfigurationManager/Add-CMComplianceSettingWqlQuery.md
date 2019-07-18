---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: 
schema: 2.0.0
---

# Add-CMComplianceSettingWqlQuery

## SYNOPSIS
Adds a compliance setting wql query

## SYNTAX

### EmptyRule (Default)
```
Add-CMComplianceSettingWqlQuery -ClassName <String> -Namespace <String> -Property <String>
 [-WhereClause <String>] -DataType <SettingDataType> [-Description <String>] -InputObject <PSObject>
 -Name <String> [-NoRule] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ValueRule
```
Add-CMComplianceSettingWqlQuery -ClassName <String> -Namespace <String> -Property <String>
 [-WhereClause <String>] [-Remediate] -DataType <SettingDataType> [-Description <String>]
 -ExpectedValue <String[]> -ExpressionOperator <RuleExpressionOperator> -InputObject <PSObject> -Name <String>
 [-NoncomplianceSeverity <NoncomplianceSeverity>] [-ReportNoncompliance] [-RuleDescription <String>]
 -RuleName <String> [-ValueRule] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ExistentialRule
```
Add-CMComplianceSettingWqlQuery -ClassName <String> -Namespace <String> -Property <String>
 [-WhereClause <String>] -DataType <SettingDataType> [-Description <String>] -Existence <ExistenceType>
 [-ExistentialRule] [-ExpectedValue <String[]>] [-ExpressionOperator <RuleExpressionOperator>]
 -InputObject <PSObject> -Name <String> [-NoncomplianceSeverity <NoncomplianceSeverity>]
 [-RuleDescription <String>] -RuleName <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1
```
PS XYZ:\>  
```

 

## PARAMETERS

### -ClassName
 

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

### -DataType
 

```yaml
Type: SettingDataType
Parameter Sets: (All)
Aliases: 
Accepted values: String, Integer, DateTime, FloatingPoint, Version, StringArray, Boolean

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
 

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

### -Existence
 

```yaml
Type: ExistenceType
Parameter Sets: ExistentialRule
Aliases: 
Accepted values: MustExist, MustNotExist, Occurs

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExistentialRule
 

```yaml
Type: SwitchParameter
Parameter Sets: ExistentialRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpectedValue
 

```yaml
Type: String[]
Parameter Sets: ValueRule
Aliases: ExpectedValues, ExpectedCount, ExpectedCounts

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: ExistentialRule
Aliases: ExpectedValues, ExpectedCount, ExpectedCounts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator
 

```yaml
Type: RuleExpressionOperator
Parameter Sets: ValueRule
Aliases: 
Accepted values: And, Or, Other, IsEquals, NotEquals, GreaterThan, LessThan, Between, NotBetween, GreaterEquals, LessEquals, BeginsWith, NotBeginsWith, EndsWith, NotEndsWith, Contains, NotContains, AllOf, OneOf, NoneOf, SetEquals, SubsetOf, ExcludesAll

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: RuleExpressionOperator
Parameter Sets: ExistentialRule
Aliases: 
Accepted values: And, Or, Other, IsEquals, NotEquals, GreaterThan, LessThan, Between, NotBetween, GreaterEquals, LessEquals, BeginsWith, NotBeginsWith, EndsWith, NotEndsWith, Contains, NotContains, AllOf, OneOf, NoneOf, SetEquals, SubsetOf, ExcludesAll

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
 

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
 

```yaml
Type: String
Parameter Sets: (All)
Aliases: SettingName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
 

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

### -NoRule
 

```yaml
Type: SwitchParameter
Parameter Sets: EmptyRule
Aliases: NoRules

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoncomplianceSeverity
 

```yaml
Type: NoncomplianceSeverity
Parameter Sets: ValueRule, ExistentialRule
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

### -Property
 

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

### -Remediate
 

```yaml
Type: SwitchParameter
Parameter Sets: ValueRule
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportNoncompliance
 

```yaml
Type: SwitchParameter
Parameter Sets: ValueRule
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleDescription
 

```yaml
Type: String
Parameter Sets: ValueRule, ExistentialRule
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
Parameter Sets: ValueRule, ExistentialRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueRule
 

```yaml
Type: SwitchParameter
Parameter Sets: ValueRule
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

### -WhereClause
 

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Management.Automation.PSObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

