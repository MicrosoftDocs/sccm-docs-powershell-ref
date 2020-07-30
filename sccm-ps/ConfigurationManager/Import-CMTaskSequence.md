---
description: Imports a Configuration Manager task sequence.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/30/2018
schema: 2.0.0
title: Import-CMTaskSequence
---

# Import-CMTaskSequence

## SYNOPSIS

Imports a Configuration Manager task sequence.

## SYNTAX

```
Import-CMTaskSequence [-IgnoreDependency] [-ImportActionType <ImportActionType>]
 [-ImportActionTypeSpec <Hashtable>] -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Import-CMTaskSequence** cmdlet imports a task sequence into Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Import a task sequence

```powershell
PS XYZ:\>Import-CMTaskSequence -ImportFilePath "\\Server1\TS\TaskSequence.zip"
```

This command imports a task sequence from the specified location.

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

Controls the behavior when a package already exists.

```yaml
Type: ImportActionType
Parameter Sets: (All)
Aliases: ImportActionForAllObjects
Accepted values: NotSet, Skip, DirectImport, Rename, Overwrite, ImportFail, IgnoreDependencyFailure, AppendDriverCategories, OverwriteIgnoreDependencyFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportActionTypeSpec
Starting in version 1906, use this parameter to specify import action type for different classes of object.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: ImportActionTypeForSpecificClass

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path

Specifies the path of the import file.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMTaskSequence](Get-CMTaskSequence.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[Set-CMTaskSequence](Set-CMTaskSequence.md)

[Copy-CMTaskSequence](Copy-CMTaskSequence.md)

[Enable-CMTaskSequence](Enable-CMTaskSequence.md)

[Disable-CMTaskSequence](Disable-CMTaskSequence.md)

[Import-CMTaskSequence](Import-CMTaskSequence.md)

[Export-CMTaskSequence](Export-CMTaskSequence.md)

[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
