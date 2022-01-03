---
description: Import a task sequence.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Import-CMTaskSequence
---

# Import-CMTaskSequence

## SYNOPSIS

Import a task sequence.

## SYNTAX

```
Import-CMTaskSequence [-IgnoreDependency] [-ImportActionType <ImportActionType>]
 [-ImportActionTypeSpec <Hashtable>] -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to import a task sequence into Configuration Manager. You can use the [Export-CMTaskSequence](Export-CMTaskSequence.md) cmdlet to export a task sequence to a .zip file.

> [!IMPORTANT]
> This cmdlet doesn't support [PowerShell 7](/powershell/sccm/overview#support-for-powershell-version-7).<!-- 6337796 --> It requires the .NET Framework instead of .NET Core that's used with PowerShell version 7.
>
> Starting in version 2103, if you try to use this cmdlet in a PowerShell version 7 session, it fails with the following error: `This cmdlet only supports the ".NET Framework" runtime.`

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import a task sequence

This command imports a task sequence from the specified location.

```powershell
Import-CMTaskSequence -ImportFilePath "\\Server1\TS\TaskSequence.zip"
```

## PARAMETERS

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

### -IgnoreDependency

Add this parameter to ignore dependencies in the task sequence.

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

If this task sequence already exists in the site, use this parameter how to handle it. By default, Configuration Manager ignores duplicates.

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

Use this parameter to specify import action type for different classes of object.

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

Specify the network path for the exported task sequence. The cmdlet imports all task sequences in the file. The path needs to specify the file, including the `.zip` extension.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FileName, FilePath, ImportFilePath

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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Export-CMTaskSequence](Export-CMTaskSequence.md)

[New-CMTaskSequence](New-CMTaskSequence.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[Set-CMTaskSequence](Set-CMTaskSequence.md)

[Copy-CMTaskSequence](Copy-CMTaskSequence.md)

[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
