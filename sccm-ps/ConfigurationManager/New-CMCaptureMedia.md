---
description: Creates capture media.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMCaptureMedia
---

# New-CMCaptureMedia

## SYNOPSIS
Creates capture media.

## SYNTAX

```
New-CMCaptureMedia [-AllowUacPrompt] -BootImage <IResultObject> -DistributionPoint <IResultObject[]> [-Force]
 [-FormatMedia] -MediaType <MediaInputType> -Path <String> [-TemporaryFolder <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCaptureMedia** cmdlets creates media used to capture an operating system deployment image from a reference computer.

NOTE: This cmdlet requires elevated permissions to run.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create capture media
```
PS XYZ:\> $BootImage = Get-CMBootImage -Name "Boot image (x64)"
PS XYZ:\> $DistributionPoint = Get-CMDistributionpoint -SiteCode CM1
PS XYZ:\> New-CMCaptureMedia -MediaType CdDvd -Path "\\server\share\CaptureMedia.iso" -BootImage $BootImage -DistributionPoint $DistributionPoint
```

The first command gets the boot image object named Boot image (x64) and stores the object in the $BootImage variable.

The second command gets the distribution point object for the site code named CM1 and stores the object in the $DistributionPoint variable.

The last command creates capture media using the BootImage stored in $BootImage, and the distribution point stored in $DistributionPoint.

## PARAMETERS

### -AllowUacPrompt
Indicates that User Account Control (UAC) prompts are allowed.

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

### -BootImage
Specifies a boot image object.
To obtain a boot image object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: BootImagePackage

Required: True
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

### -DistributionPoint
Specifies an array of distribution point objects.
To obtain a distribution point object, use the [Get-CMDistributionPoint](Get-CMDistributionPoint.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DistributionPoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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

### -FormatMedia
Indicates that the cmdlet formats the removable USB drive (FAT32), and makes it bootable.

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

### -MediaType
Specifies the media mode.
Valid values are:

- Usb
- CdDvd
- Hd

```yaml
Type: MediaInputType
Parameter Sets: (All)
Aliases:
Accepted values: Usb, CdDvd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the name and path where the output files are written.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MediaPath, OutputPath, DriveName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemporaryFolder
{{ Fill TemporaryFolder Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: TemporaryDirectory, StagingArea

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

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)


