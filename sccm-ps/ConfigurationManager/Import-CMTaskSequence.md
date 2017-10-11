---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: B63CE9E9-C730-4BAD-A561-4B09B2FEB4D2
online version: https://go.microsoft.com/fwlink/?linkid=834082
schema: 2.0.0
---

# Import-CMTaskSequence

## SYNOPSIS
Imports a task sequence.

## SYNTAX

```
Import-CMTaskSequence [-IgnoreDependency] [-ImportActionType <ImportActionType>] -Path <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMTaskSequence** cmdlet imports a task sequence into Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Import a task sequence
```
PS C:\>Import-CMTaskSequence -ImportFilePath "\\Server1\TS\TaskSequence.zip"
```

This command imports a task sequence from the specified location.

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

### -IgnoreDependency
Indicates that the import process ignores dependencies in the task sequence.

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

### -ImportActionType
 

```yaml
Type: ImportActionType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Skip, DirectImport, Rename, Overwrite, ImportFail, IgnoreDependencyFailure, AppendDriverCategories, OverwriteIgnoreDependencyFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
 

```yaml
Type: String
Parameter Sets: (All)
Aliases: ImportFilePath

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

[Disable-CMTaskSequence](Disable-CMTaskSequence.md)

[Enable-CMTaskSequence](Enable-CMTaskSequence.md)

[Export-CMTaskSequence](Export-CMTaskSequence.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[New-CMTaskSequence](New-CMTaskSequence.md)

[Remove-CMTaskSequence](Remove-CMTaskSequence.md)

[Set-CMTaskSequence](Set-CMTaskSequence.md)


