---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/01/2021
schema: 2.0.0
title: New-CMBootImage
---

# New-CMBootImage

## SYNOPSIS

Create a custom boot image.

## SYNTAX

```
New-CMBootImage [-Description <String>] -Index <Int32> -Name <String> -Path <String> [-Version <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a custom Windows Preinstallation Environment (Windows PE) OS boot image. By default, Configuration Manager includes two boot images for x86 and x64 architectures. For more information, see [Manage boot images with Configuration Manager](/mem/configmgr/osd/get-started/manage-boot-images).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a custom boot image

This command creates a custom boot image. It specifies a source path for its WIM file, an index value, a name, a version, and a description.

```powershell
New-CMBootImage -Path "\\Server99.Contoso.com\SMS_CCC\osd\boot\x64\boot.wim" -Index 1 -Name "Custom boot image" -Version "11" -Description "WinPE Boot Image x64 Approved 9/1/2012"
```

## PARAMETERS

### -Description

Specify an optional description of a boot image to help you identify it.

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

### -Index

Specify the index of the image in the WinPE file to use for this boot image.

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

Specify the name of the boot image.

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

Specify the network path of the original WIM file for the boot image.

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

Specify the version of the boot image. This value isn't the OS version, but a string that you manage.

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

### None
## OUTPUTS

### IResultObject#SMS_BootImagePackage
## NOTES

For more information on this return object and its properties, see [SMS_BootImagePackage server WMI class](/mem/configmgr/develop/reference/osd/sms_bootimagepackage-server-wmi-class).

## RELATED LINKS

[Get-CMBootImage](Get-CMBootImage.md)

[Remove-CMBootImage](Remove-CMBootImage.md)

[Set-CMBootImage](Set-CMBootImage.md)

[Manage boot images with Configuration Manager](/mem/configmgr/osd/get-started/manage-boot-images)
