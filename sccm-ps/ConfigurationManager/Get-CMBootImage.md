---
author: aczechowski
description: Gets an operating system boot image.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMBootImage
titleSuffix: Configuration Manager
---

# Get-CMBootImage

## SYNOPSIS
Gets an operating system boot image.

## SYNTAX

### SearchByName (Default)
```
Get-CMBootImage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBootImage -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBootImage** cmdlet gets a Windows Preinstallation Environment (PE) operating system boot image that Microsoft System Center Configuration Manager can use to deploy an operating system.

Operating system boot images are .wim format files.
These files contain a compressed set of reference files and folders that are required to successfully install and configure an operating system image.
By default, System Center Configuration Manager includes both x86 and x64 boot images.

You must run the **Get-CMBootImage** cmdlet on the computer that is running the Systems Management Server (SMS) provider.
The computer account of the computer that is running the SMS provider must have Read and Write access to the source package of the boot image.
For more information about the SMS provider, see [Planning for the SMS Provider in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=263566) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a boot image by using its ID
```
PS XYZ:\> Get-CMBootImage -Id "c0eb2912-0de8-4a2a-9c77-603b35bcf7e4"
```

This command gets a boot image by using its ID.

### Example 2: Get a boot image by using its name
```
PS XYZ:\> Get-CMBootImage -Name "SMS_BootImagePackage"
```

This command gets a boot image by using its name.

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
Specifies an array of boot image identifiers.

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
Specifies a name of a boot image.

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

[Planning for the SMS Provider in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=263566)

[New-CMBootImage](New-CMBootImage.md)

[Remove-CMBootImage](Remove-CMBootImage.md)

[Set-CMBootImage](Set-CMBootImage.md)


