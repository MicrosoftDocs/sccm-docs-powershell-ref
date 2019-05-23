---
title: Import-CMTaskSequence
titleSuffix: Configuration Manager
description: Imports a Configuration Manager task sequence.
ms.date: 11/30/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Import-CMTaskSequence

## SYNOPSIS

Imports a Configuration Manager task sequence.

## SYNTAX

```powershell
Import-CMTaskSequence [-IgnoreDependency] [-ImportActionType <ImportActionType>] -Path <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Import-CMTaskSequence** cmdlet imports a task sequence into Microsoft System Center Configuration Manager.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


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
Aliases: 
Accepted values: NotSet, Skip, DirectImport, Rename, Overwrite, ImportFail, IgnoreDependencyFailure, AppendDriverCategories, OverwriteIgnoreDependencyFailure

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[New-CMTaskSequence](Net-CMTaskSequence.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[Set-CMTaskSequence](Set-CMTaskSequence.md)

[Copy-CMTaskSequence](Copy-CMTaskSequence.md)

[Enable-CMTaskSequence](Enable-CMTaskSequence.md)

[Disable-CMTaskSequence](Disable-CMTaskSequence.md)

[Import-CMTaskSequence](Import-CMTaskSequence.md)

[Export-CMTaskSequence](Export-CMTaskSequence.md)

[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
