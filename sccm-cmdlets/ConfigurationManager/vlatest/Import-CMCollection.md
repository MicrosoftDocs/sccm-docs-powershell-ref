---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: D3A42200-DE43-4FCD-949A-10FCAE145DF5
---

# Import-CMCollection

## SYNOPSIS
Imports a collection.

## SYNTAX

```
Import-CMCollection [-ImportFilePath] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMCollection** cmdlet imports a previously exported collection into Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Import a collection
```
PS C:\> Import-CMCollection -ImportFilePath "c:\path\collection.mof"
```

This command imports the collection defined in the collection.mof file.

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

### -ImportFilePath
Specifies the full path of the import (MOF) file for the collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

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

[Get-CMCollection](./Get-CMCollection.md)

[Export-CMCollection](./Export-CMCollection.md)

[New-CMCollection](./New-CMCollection.md)

[Remove-CMCollection](./Remove-CMCollection.md)

[Set-CMCollection](./Set-CMCollection.md)


