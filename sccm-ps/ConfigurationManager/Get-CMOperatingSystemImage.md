---
author: aczechowski
description: Gets operating system images.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMOperatingSystemImage
titleSuffix: Configuration Manager
---

# Get-CMOperatingSystemImage

## SYNOPSIS
Gets operating system images.

## SYNTAX

### SearchByName (Default)
```
Get-CMOperatingSystemImage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMOperatingSystemImage -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOperatingSystemImage** cmdlet gets one or more operating system images on a Microsoft System Center Configuration Manager site.
Operating system images are .wim format files and represent a compressed collection of reference files and folders that System Center Configuration Manager requires to successfully install and configure an operating system on a computer.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get an operating system image
```
PS XYZ:\> Get-CMOperatingSystemImage -Name "OSImagePkg01" -SecuredScopeNames "SecScope02"
```

This command gets the operating system image named OSImagePkg01 for the security scope named SecScope02.

## PARAMETERS

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

### -Id
Specifies an array of IDs of operating system images.

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
Specifies the name of an operating system image.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMOperatingSystemImage](New-CMOperatingSystemImage.md)

[Set-CMOperatingSystemImage](Set-CMOperatingSystemImage.md)

[Remove-CMOperatingSystemImage](Remove-CMOperatingSystemImage.md)

[Get-CMOperatingSystemImageUpdateSchedule](Get-CMOperatingSystemImageUpdateSchedule.md)


