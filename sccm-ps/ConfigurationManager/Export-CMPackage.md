---
description: Export a legacy package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Export-CMPackage
---

# Export-CMPackage

## SYNOPSIS

Export a legacy package.

## SYNTAX

### SearchByValue (Default)
```
Export-CMPackage [-Comment <String>] -FileName <String> [-Force] -InputObject <IResultObject>
 [-WithContent <Boolean>] [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Export-CMPackage [-Comment <String>] -FileName <String> [-Force] -Id <String> [-WithContent <Boolean>]
 [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchPackageByNameMandatory
```
Export-CMPackage [-Comment <String>] -FileName <String> [-Force] -Name <String> [-WithContent <Boolean>]
 [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to export a Configuration Manager legacy package. You can use the [Import-CMPackage](Import-CMPackage.md) cmdlet to import a legacy package to another site.

Configuration Manager current branch continues to support packages and programs that were used in Configuration Manager 2007. For more information, see [Packages and programs in Configuration Manager](/mem/configmgr/apps/deploy-use/packages-and-programs).

> [!IMPORTANT]
> This cmdlet doesn't support [PowerShell 7](/powershell/sccm/overview#support-for-powershell-version-7).<!-- 6337796 --> It requires the .NET Framework instead of .NET Core that's used with PowerShell version 7.
>
> Starting in version 2103, if you try to use this cmdlet in a PowerShell version 7 session, it fails with the following error: `This cmdlet only supports the ".NET Framework" runtime.`

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Export a package by using an ID

This command exports a package that has the ID **ST120001** to a network path.

```powershell
Export-CMPackage -Id "ST120001" -FileName "\\Deploy01\ExportPackages\ST120001.zip"
```

### Example 2: Export a package by using a variable

The first command gets the package that has the ID **ST120001**, and then stores it in the variable **$DeplObj**. The second command exports the package to the network path by using the variable.

```powershell
$DeplObj = Get-CMPackage -Id "ST120001"
Export-CMPackage - "ST120001" -FileName "\\Deploy01\ExportPackages\ST120001.zip" -InputObject $DeplObj
```

## PARAMETERS

### -Comment

Specify an optional administrator comment. This comment displays in the Import Package Wizard.

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

### -FileName

Specify the network path for the package. The path needs to specify the file, including the `.zip` extension.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath, ExportFilePath, Path

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

Specify the package ID to export. This value is the standard package ID, for example `XYZ00123`.

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

Specify a package object to export. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

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

Specify the name of a package to export.

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

Set this parameter to **$true** to export all content for the package and dependencies.

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

Set this parameter to **$true** to export all package dependencies.

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

[Import-CMPackage](Import-CMPackage.md)

[Get-CMPackage](Get-CMPackage.md)

[New-CMPackage](New-CMPackage.md)

[Remove-CMPackage](Remove-CMPackage.md)

[Set-CMPackage](Set-CMPackage.md)
