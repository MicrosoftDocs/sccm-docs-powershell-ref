---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
online version:
schema: 2.0.0
---

# Invoke-CMAnalyzePackage

## SYNOPSIS

Analyze a package to convert to an application.

## SYNTAX

### SearchByName (Default)
```
Invoke-CMAnalyzePackage [-Name <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMAnalyzePackage -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValue
```
Invoke-CMAnalyzePackage -InputObject <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to analyze a package to convert to an application. This cmdlet invokes the package conversion manager tools that are integrated with Configuration Manager. For more information, see [Package Conversion Manager](/mem/configmgr/apps/pcm/package-conversion-manager).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Invoke-CMAnalyzePackage -Name $packageName
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

### -Id

Specify a package ID to analyze. For example, `XYZ006C5`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: IDs, PackageID, PackageIDs

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Applies to version 2010 and later. Specify a package object to analyze. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

This parameter replaces the previous **Package** parameter.

```yaml
Type: IResultObject[]
Parameter Sets: SetByValue
Aliases: Packages, Package

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify a package name to analyze.

```yaml
Type: String[]
Parameter Sets: SearchByName
Aliases: Names, PackageName, PackageNames

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

## OUTPUTS

### System.Object
## NOTES

Starting in version 2010, the **Package** parameter was removed from this cmdlet. Pipe the package object, or use the **InputObject** parameter.

## RELATED LINKS

[Invoke-CMConvertPackage](Invoke-CMConvertPackage.md)

[Get-CMPackage](Get-CMPackage.md)

[Package Conversion Manager](/mem/configmgr/apps/pcm/package-conversion-manager)
