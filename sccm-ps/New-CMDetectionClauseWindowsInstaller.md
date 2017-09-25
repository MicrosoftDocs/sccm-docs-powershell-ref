---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMDetectionClauseWindowsInstaller

## SYNOPSIS
Creates a detection clause windows installer

## SYNTAX

### Value
```
New-CMDetectionClauseWindowsInstaller -ExpectedValue <String[]> -ExpressionOperator <RuleExpressionOperator>
 -ProductCode <Guid> [-PropertyType <MSIProperty>] [-Value] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseWindowsInstaller -ProductCode <Guid> [-Existence] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
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
{{Fill Existence Description}}

```yaml
Type: SwitchParameter
Parameter Sets: Existence
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpectedValue
{{Fill ExpectedValue Description}}

```yaml
Type: String[]
Parameter Sets: Value
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator
{{Fill ExpressionOperator Description}}

```yaml
Type: RuleExpressionOperator
Parameter Sets: Value
Aliases: 
Accepted values: IsEquals, NotEquals, GreaterEquals, GreaterThan, LessEquals, LessThan

Required: True
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

### -ProductCode
{{Fill ProductCode Description}}

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyType
{{Fill PropertyType Description}}

```yaml
Type: MSIProperty
Parameter Sets: Value
Aliases: 
Accepted values: ProductVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
{{Fill Value Description}}

```yaml
Type: SwitchParameter
Parameter Sets: Value
Aliases: ValueRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

