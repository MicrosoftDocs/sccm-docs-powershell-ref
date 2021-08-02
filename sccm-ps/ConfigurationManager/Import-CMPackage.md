---
description: Import a legacy package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Import-CMPackage
---

# Import-CMPackage

## SYNOPSIS

Import a legacy package.

## SYNTAX

```
Import-CMPackage [-ImportActionType <ImportActionType>] -ImportFilePath <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to import a Configuration Manager legacy package. You can use the [Export-CMPackage](Export-CMPackage.md) cmdlet to export a legacy package to a .zip file.

Configuration Manager current branch continues to support packages and programs that were used in Configuration Manager 2007. For more information, see [Packages and programs in Configuration Manager](/mem/configmgr/apps/deploy-use/packages-and-programs).

> [!IMPORTANT]
> This cmdlet doesn't support [PowerShell 7](/powershell/sccm/overview#support-for-powershell-version-7).<!-- 6337796 --> It requires the .NET Framework instead of .NET Core that's used with PowerShell version 7.
>
> Starting in version 2103, if you try to use this cmdlet in a PowerShell version 7 session, it fails with the following error: `This cmdlet only supports the ".NET Framework" runtime.`

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import a package

This command imports a package from a network path.

```powershell
Import-CMPackage -ImportFilePath "\\Deploy01\ExportPackages"
```

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

### -ImportActionType

If this package already exists in the site, use this parameter how to handle it. By default, Configuration Manager ignores duplicates.

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

Specify the network path for the exported package. The cmdlet imports all packages in the file. The path needs to specify the file, including the `.zip` extension.

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

[Export-CMPackage](Export-CMPackage.md)

[Get-CMPackage](Get-CMPackage.md)

[New-CMPackage](New-CMPackage.md)

[Remove-CMPackage](Remove-CMPackage.md)

[Set-CMPackage](Set-CMPackage.md)
