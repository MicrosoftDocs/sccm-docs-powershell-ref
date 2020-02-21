---
author: aczechowski
description: Imports a driver package.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Import-CMDriverPackage
titleSuffix: Configuration Manager
---

# Import-CMDriverPackage

## SYNOPSIS
Imports a driver package.

## SYNTAX

```
Import-CMDriverPackage -ImportFilePath <String> [-ImportActionType <ImportActionType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMDriverPackage** cmdlet imports a driver packages to Microsoft System Center Configuration Manager.
You can use the [Export-CMDriverPackage](Export-CMDriverPackage.md) cmdlet to export a driver package to a .zip file.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Import a driver package
```
PS XYZ:\>Import-CMDriverPackage -ImportFilePath "\\Contoso02\main\driverpackages\DriverPackage.zip"
```

This command imports a driver package from the import file named DriverPackage.zip.

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

### -ImportFilePath
Specifies the Universal Naming Convention (UNC) path of the import file.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Export-CMDriverPackage](Export-CMDriverPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[New-CMDriverPackage](New-CMDriverPackage.md)

[Remove-CMDriverPackage](Remove-CMDriverPackage.md)

[Set-CMDriverPackage](Set-CMDriverPackage.md)


