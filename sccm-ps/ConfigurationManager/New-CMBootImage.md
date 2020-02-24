---
author: aczechowski
description: Adds a new operating system boot image.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMBootImage
titleSuffix: Configuration Manager
---

# New-CMBootImage

## SYNOPSIS
Adds a new operating system boot image.

## SYNTAX

```
New-CMBootImage -Path <String> -Index <Int32> -Name <String> [-Version <String>] [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMBootImage** cmdlet adds a new Windows Preinstallation Environment (Windows PE) operating system boot image to Microsoft System Center Configuration Manager.
Operating system images are .wim format files.
These files contain a compressed set of reference files and folders that are required to successfully install and configure a boot image on a computer.
By default, System Center Configuration Manager includes both x86 and x64 operating system images.

You must run **New-CMBootImage** on the computer that is running the Systems Management Server (SMS) provider.
The computer account of the computer that is running the SMS provider must have Read and Write access to the package source of the boot image.
For more information about the SMS provider, see [Planning for the SMS Provider in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg712282(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a new boot image object
```
PS XYZ:\> New-CMBootImage -Path "\\Server99.Contoso.com\SMS_CCC\osd\boot\i386\boot.wim" -Index 1 -Name "WinPE Boot Image" -Version 11 -Description "WinPE Boot Image x86 Approved 9/1/2012"
```

This command creates a new boot image object and provides it with a source path for its WIM file, an index value, a name, an operating system version, and a description.

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

### -Description
Specifies a description of the boot image.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

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

### -Index
Specifies an index.
An index is the number of an image in a .wim file.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImageIndex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a new boot image.

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

### -Path
Specifies the location of the original WIM file for the boot image.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ImagePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies the version of the boot image.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Planning for the SMS Provider in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg712282(v=technet.10))

[Get-CMBootImage](Get-CMBootImage.md)

[Remove-CMBootImage](Remove-CMBootImage.md)

[Set-CMBootImage](Set-CMBootImage.md)


