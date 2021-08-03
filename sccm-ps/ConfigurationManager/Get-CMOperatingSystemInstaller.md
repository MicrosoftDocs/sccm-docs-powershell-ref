---
description: Gets OS upgrade packages
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: Get-CMOperatingSystemInstaller
---

# Get-CMOperatingSystemInstaller

## SYNOPSIS
Gets OS upgrade packages.

## SYNTAX

### SearchByName (Default)
```
Get-CMOperatingSystemInstaller [-Name <String>] [-Reload] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMOperatingSystemInstaller -Id <String> [-Reload] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMOperatingSystemInstaller** cmdlet gets one or more OS upgrade packages. An OS upgrade package contains all the files that Configuration Manager needs to install a Windows OS on a reference computer.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an OS upgrade package

This command gets the OS upgrade package named OSInstPkg01 for the security scope named SecScope02.

```powershell
Get-CMOperatingSystemInstaller -Name "OSInstPkg01"-SecuredScopeNames "SecScope02"
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
Specifies an array of IDs of OS upgrade packages.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of an OS upgrade package.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Reload

Applies to version 2006 and later. If you change the image properties using an external tool, use this option to reload the information in the site database.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ReloadImage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_OperatingSystemInstallPackage
### IResultObject#SMS_OperatingSystemInstallPackage
## NOTES

## RELATED LINKS

[New-CMOperatingSystemInstaller](New-CMOperatingSystemInstaller.md)

[Remove-CMOperatingSystemInstaller](Remove-CMOperatingSystemInstaller.md)

[Set-CMOperatingSystemInstaller](Set-CMOperatingSystemInstaller.md)


