---
description: Imports a driver package.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Import-CMDriverPackage
---

# Import-CMDriverPackage

## SYNOPSIS
Imports a driver package.

## SYNTAX

```
Import-CMDriverPackage -ImportFilePath <String> [-ImportActionType <ImportActionType>]
 [-ImportActionTypeSpec <Hashtable>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMDriverPackage** cmdlet imports a driver packages to Configuration Manager.
You can use the [Export-CMDriverPackage](Export-CMDriverPackage.md) cmdlet to export a driver package to a .zip file.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Import a driver package

This command imports a driver package from the import file named DriverPackage.zip.

```PowerShell
Import-CMDriverPackage -ImportFilePath "\\Contoso02\main\driverpackages\DriverPackage.zip"
```

### Example 2: Specify import action type

This example specifies an import action type for different classes of object

```PowerShell
$classVsAction = @{"SMS_Driver" = [Microsoft.ConfigurationManagement.AdminConsole.MigrationAssistant.ImportActionType]::AppendDriverCategories}
Import-CMDriverPackage -ImportFilePath $filePath -ImportActionTypeSpec $classVsAction
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

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Export-CMDriverPackage](Export-CMDriverPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[New-CMDriverPackage](New-CMDriverPackage.md)

[Remove-CMDriverPackage](Remove-CMDriverPackage.md)

[Set-CMDriverPackage](Set-CMDriverPackage.md)


