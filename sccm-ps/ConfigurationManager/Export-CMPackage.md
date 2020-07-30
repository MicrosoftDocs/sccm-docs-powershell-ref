---
description: Exports a Configuration Manager package.
external help file: AdminUI.PS.AppModel.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Export-CMPackage
---

# Export-CMPackage

## SYNOPSIS
Exports a Configuration Manager package.

## SYNTAX

### SearchByValue (Default)
```
Export-CMPackage -InputObject <IResultObject> -FileName <String> [-WithDependence <Boolean>]
 [-WithContent <Boolean>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Export-CMPackage -Id <String> -FileName <String> [-WithDependence <Boolean>] [-WithContent <Boolean>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchPackageByNameMandatory
```
Export-CMPackage -Name <String> -FileName <String> [-WithDependence <Boolean>] [-WithContent <Boolean>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMPackage** cmdlet exports a Configuration Manager package.
You can use this cmdlet in Configuration Manager to create a package of collections, queries, or reports and then export that package so that you can later deploy these items to a different location.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Export a package by using an ID
```
PS XYZ:\>Export-CMPackage -Id "ST120001" -ExportFilePath "\\Deploy01\ExportPackages"
```

This command exports a package that has the ID ST120001 to the output path \\\\Deploy01\ExportPackages.

### Example 2: Export a package by using a variable
```
PS XYZ:\> $DeplObj = Get-CMPackage -Id "ST120001"
PS XYZ:\> Export-CMPackage - "ST120001" -ExportFilePath"\\Deploy01\ExportPackages" -InputObject $DeplObj
```

The first command gets the package that has the ID ST120001, and then stores it in the variable $DeplObj.

The second command exports the package to the path \\\\Deploy01\ExportPackages by using the $DeplObj variable.

## PARAMETERS

### -Comment
```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
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

### -FileName
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExportFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
{{ Fill Force Description }}

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

### -Id
Specifies an array of IDs for packages.

```yaml
Type: String
Parameter Sets: SearchPackageByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the package that you export by using a Configuration Manager package object.
To obtain a package object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a package.

```yaml
Type: String
Parameter Sets: SearchPackageByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WithContent
Indicates whether to include content in the package.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WithDependence
Indicates whether to include dependencies in the package.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Import-CMPackage](Import-CMPackage.md)

[Get-CMPackage](Get-CMPackage.md)

[New-CMPackage](New-CMPackage.md)

[Remove-CMPackage](Remove-CMPackage.md)

[Set-CMPackage](Set-CMPackage.md)


