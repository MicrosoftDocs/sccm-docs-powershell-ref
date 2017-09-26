---
external help file: AdminUI.PS.Common.dll-Help.xml
ms.assetid: 852B2CB4-10AC-482F-8B2D-C4654431DEF5
online version: https://go.microsoft.com/fwlink/?linkid=833641
schema: 2.0.0
---

# New-CMEmbeddedObjectInstance

## SYNOPSIS
Creates an embedded object instance.

## SYNTAX

```
New-CMEmbeddedObjectInstance -ClassName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMEmbeddedObjectInstance** creates an instance of an embedded object.

## EXAMPLES

### Example 1: Create an embedded object instance
```
PS ABC:\> New-CMEmbeddedObjectInstance -ClassName "SMS_OS_Details"
```

This command creates an embedded object instance by using the class named SMS_OS_Details.

## PARAMETERS

### -ClassName
Specifies the name of a Configuration Manager class.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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
Default value: False
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

[New-CMEmbeddedProperty](New-CMEmbeddedProperty.md)

[New-CMEmbeddedPropertyList](New-CMEmbeddedPropertyList.md)
