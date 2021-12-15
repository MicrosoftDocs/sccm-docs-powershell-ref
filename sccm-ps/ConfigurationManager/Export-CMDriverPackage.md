---
description: Export a driver package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Export-CMDriverPackage
---

# Export-CMDriverPackage

## SYNOPSIS

Export a driver package.

## SYNTAX

### SearchPackageByNameMandatory (Default)
```
Export-CMDriverPackage [-Comment <String>] -ExportFilePath <String> [-Force] -Name <String>
 [-WithContent <Boolean>] [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Export-CMDriverPackage [-Comment <String>] -ExportFilePath <String> [-Force] -InputObject <IResultObject>
 [-WithContent <Boolean>] [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Export-CMDriverPackage [-Comment <String>] -ExportFilePath <String> [-Force] -Id <String>
 [-WithContent <Boolean>] [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to export driver packages. You can use the [Import-CMDriverPackage](Import-CMDriverPackage.md) cmdlet to import a driver package to the site.

> [!IMPORTANT]
> This cmdlet doesn't support [PowerShell 7](/powershell/sccm/overview#support-for-powershell-version-7).<!-- 6337796 --> It requires the .NET Framework instead of .NET Core that's used with PowerShell version 7.
>
> Starting in version 2103, if you try to use this cmdlet in a PowerShell version 7 session, it fails with the following error: `This cmdlet only supports the ".NET Framework" runtime.`

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Export a driver package

This command exports the driver package named DrvPkg01 to the export file DriverPackage01.zip.

```powershell
Export-CMDriverPackage -Name "DrvPkg01" -ExportFilePath "\\Contoso02\DriverPackages\DriverPackage01.zip"
```

## PARAMETERS

### -Comment

Specify an optional administrator comment. This comment displays in the Import Driver Package Wizard.

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

### -ExportFilePath

Specify the network path for the driver package. The path needs to specify the file, including the `.zip` extension.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FileName, FilePath, Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Run the command without asking for confirmation.

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

Specify the driver package ID to export. This value is the standard package ID, for example `XYZ00123`.

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

Specify a driver package object to export. To get this object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a driver package to export.

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

Set this parameter to **$true** to export all content for the driver package and drivers.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ExportAllContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WithDependence

Set this parameter to **$true** to export all associated drivers.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ExportAssociateDrivers

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Import-CMDriverPackage](Import-CMDriverPackage.md)

[New-CMDriverPackage](New-CMDriverPackage.md)

[Remove-CMDriverPackage](Remove-CMDriverPackage.md)

[Set-CMDriverPackage](Set-CMDriverPackage.md)
