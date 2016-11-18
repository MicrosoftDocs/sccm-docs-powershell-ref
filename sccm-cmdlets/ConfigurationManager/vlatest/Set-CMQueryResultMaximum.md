---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 1A0A53E9-FBFD-4DE8-9E06-B089EA04B244
---

# Set-CMQueryResultMaximum

## SYNOPSIS
Changes the setting for the query result maximum.

## SYNTAX

```
Set-CMQueryResultMaximum [-Maximum] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMQueryResultMaximum** cmdlet changes the setting for the maximum number of rows that a Microsoft System Center Configuration Manager query can return.

## EXAMPLES

### Example 1: Set the query result maximum
```
PS C:\>Set-CMQueryResultMaximum -Maximum 2500
```

This command sets the maximum number of rows that a Configuration Manager report query can return to 2500.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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

### -Maximum
Specifies the maximum number of rows that a Configuration Manager report query can return.
The default value is 10,000.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMQueryResultMaximum](./Get-CMQueryResultMaximum.md)


