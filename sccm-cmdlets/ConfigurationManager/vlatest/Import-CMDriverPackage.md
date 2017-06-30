---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: 2E251111-93BB-4D25-AD73-C7C1C316E253
online version: https://go.microsoft.com/fwlink/?linkid=834062
schema: 2.0.0
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
You can use the [Export-CMDriverPackage](./Export-CMDriverPackage.md) cmdlet to export a driver package to a .zip file.

## EXAMPLES

### Example 1: Import a driver package
```
PS C:\>Import-CMDriverPackage -ImportFilePath "\\Contoso02\main\driverpackages\DriverPackage.zip"
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
{{Fill ImportActionType Description}}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Export-CMDriverPackage](./Export-CMDriverPackage.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)

[New-CMDriverPackage](./New-CMDriverPackage.md)

[Remove-CMDriverPackage](./Remove-CMDriverPackage.md)

[Set-CMDriverPackage](./Set-CMDriverPackage.md)


