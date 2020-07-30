---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMTSRule

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### VariableOnly (Default)
```
New-CMTSRule -Variable <Hashtable> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ComputerCondition
```
New-CMTSRule [-AssetTag <String>] [-MacAddress <String>] [-SerialNumber <String>] [-Uuid <String>]
 -Variable <Hashtable> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### LocationCondition
```
New-CMTSRule [-DefaultGateway <String>] -Variable <Hashtable> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MakeModelCondition
```
New-CMTSRule [-Make <String>] [-Model <String>] -Variable <Hashtable> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VariableCondition
```
New-CMTSRule [-ReferencedVariableName <String>] [-ReferencedVariableOperator <VariableOperatorType>]
 [-ReferencedVariableValue <String>] -Variable <Hashtable> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AssetTag
{{ Fill AssetTag Description }}

```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultGateway
{{ Fill DefaultGateway Description }}

```yaml
Type: String
Parameter Sets: LocationCondition
Aliases:

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

### -MacAddress
{{ Fill MacAddress Description }}

```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Make
{{ Fill Make Description }}

```yaml
Type: String
Parameter Sets: MakeModelCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Model
{{ Fill Model Description }}

```yaml
Type: String
Parameter Sets: MakeModelCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableName
{{ Fill ReferencedVariableName Description }}

```yaml
Type: String
Parameter Sets: VariableCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableOperator
{{ Fill ReferencedVariableOperator Description }}

```yaml
Type: VariableOperatorType
Parameter Sets: VariableCondition
Aliases:
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual, Like

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableValue
{{ Fill ReferencedVariableValue Description }}

```yaml
Type: String
Parameter Sets: VariableCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SerialNumber
{{ Fill SerialNumber Description }}

```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uuid
{{ Fill Uuid Description }}

```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable
{{ Fill Variable Description }}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Variables

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_Rule

## NOTES

## RELATED LINKS
