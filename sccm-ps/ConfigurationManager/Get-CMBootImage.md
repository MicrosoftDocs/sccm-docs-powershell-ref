---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/01/2021
schema: 2.0.0
title: Get-CMBootImage
---

# Get-CMBootImage

## SYNOPSIS

Get an OS boot image.

## SYNTAX

### SearchByName (Default)
```
Get-CMBootImage [-Name <String>] [-Reload] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBootImage -Id <String> [-Reload] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a Windows Preinstallation Environment (PE) OS boot image that Configuration Manager uses to deploy an OS. By default, Configuration Manager includes both x86 and x64 boot images. For more information, see [Manage boot images with Configuration Manager](/mem/configmgr/osd/get-started/manage-boot-images).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a boot image by using its ID

This command gets a boot image by using its ID.

```Powershell
Get-CMBootImage -Id "XYZ00002"
```

### Example 2: List all boot images

This command gets all boot images at the site and lists several properties in a table format.

```powershell
Get-CMBootImage | Select-Object PackageId, Name, ImageOSVersion, ProductionClientVersion, InputLocale | Format-Table
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

Specify a boot image ID to get. This value is a standard package ID, for example, `XYZ00002`.

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

Specify the name of a boot image to get.

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

### -Reload

Applies to version 2006 and later. If the version of the Windows ADK components in the boot image are out of date, use this parameter to reload this boot image with the current Windows PE version from the Windows ADK. For more information, see [Update distribution points with the boot image](/mem/configmgr/osd/get-started/manage-boot-images#update-distribution-points-with-the-boot-image).

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

### IResultObject[]#SMS_BootImagePackage
### IResultObject#SMS_BootImagePackage
## NOTES

For more information on this return object and its properties, see [SMS_BootImagePackage server WMI class](/mem/configmgr/develop/reference/osd/sms_bootimagepackage-server-wmi-class).

## RELATED LINKS

[New-CMBootImage](New-CMBootImage.md)

[Remove-CMBootImage](Remove-CMBootImage.md)

[Set-CMBootImage](Set-CMBootImage.md)

[Manage boot images with Configuration Manager](/mem/configmgr/osd/get-started/manage-boot-images)
