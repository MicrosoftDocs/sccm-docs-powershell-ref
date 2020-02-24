---
author: aczechowski
description: Creates prestaged media.
external help file:
manager: dougeby
Module Name: AdminUI.PS.Osd
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMPrestagedMedia
titleSuffix: Configuration Manager
---

# New-CMPrestagedMedia

## SYNOPSIS
Creates prestaged media.

## SYNTAX

## DESCRIPTION
The **New-CMPrestagedMedia** cmdlet creates a file to prestage on a new hard drive that includes an operating system image.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create prestaged media
```
PS XYZ:\> $ManagementPoint = Get-CMManagementPoint -SiteSystemServerName "dist01.contoso.com" -SiteCode "CM1"
PS XYZ:\> $BootImage = Get-CMBootImage -Name "BootImage01"
PS XYZ:\> $DistributionPoint = Get-CMDistributionPoint -SiteSystemServerName "dist01.contoso.com" -SiteCode "CM1"
PS XYZ:\> $OSImage = Get-CMOperatingSystemImage -Name "OSImagePkg01"
PS XYZ:\> New-CMPrestagedMedia -MediaMode Dynamic -Path "\\server\share\PrestargedMedia.wim" -BootImage $BootImage -DistributionPoint $DistributionPoint -ManagementPoint $ManagementPoint -OperatingSystemImage $OSImage
```

The first command gets the management point object for the site system server named dist01.contoso.com with the site code CM1 and stores the object in the $ManagementPoint variable.

The second command gets the boot image object named BootImage01 and stores the object in the $BootImage variable.

The third command gets the Distribution point object for the site system server named dist01.contoso.com with the site code CM1 and stores the object in the $DistributionPoint variable.

The fourth command gets the operating system image object named OSImagePkg01 and stores the object inthe $OSImage variable.

The last command creates a dynamic prestaged media file named PrestargedMedia.wim with the boot image stored in $BootImage, the distribution point stored in $DistributionPoint, the management point stored in $ManagementPoint, and the operating system image stored in $OSImage.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMPackage](Get-CMPackage.md)


