---
description: Gets an operating system boot image.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMBootImage
---

# Get-CMBootImage

## SYNOPSIS
Gets an operating system boot image.

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
The **Get-CMBootImage** cmdlet gets a Windows Preinstallation Environment (PE) operating system boot image that Configuration Manager can use to deploy an operating system.

Operating system boot images are .wim format files.
These files contain a compressed set of reference files and folders that are required to successfully install and configure an operating system image.
By default, Configuration Manager includes both x86 and x64 boot images.

You must run the **Get-CMBootImage** cmdlet on the computer that is running the Systems Management Server (SMS) provider.
The computer account of the computer that is running the SMS provider must have Read and Write access to the source package of the boot image.
For more information about the SMS provider, see [Planning for the SMS Provider in Configuration Manager](https://docs.microsoft.com/mem/configmgr/core/plan-design/hierarchy/plan-for-the-sms-provider).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a boot image by using its ID

This command gets a boot image by using its ID.

```Powershell
Get-CMBootImage -Id "c0eb2912-0de8-4a2a-9c77-603b35bcf7e4"
```

### Example 2: Get a boot image by using its name

This command gets a boot image by using its name.

```powershell
Get-CMBootImage -Name "SMS_BootImagePackage"
```

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

### -Reload

Applies to version 2006 and later. If the version of the Windows ADK components in the boot image are out of date, use this parameter to reload this boot image with the current Windows PE version from the Windows ADK. For more information on this process, see [Update distribution points with the boot image](https://docs.microsoft.com/mem/configmgr/osd/get-started/manage-boot-images#update-distribution-points-with-the-boot-image).

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

## RELATED LINKS

[Planning for the SMS Provider in Configuration Manager](https://docs.microsoft.com/mem/configmgr/core/plan-design/hierarchy/plan-for-the-sms-provider)

[New-CMBootImage](New-CMBootImage.md)

[Remove-CMBootImage](Remove-CMBootImage.md)

[Set-CMBootImage](Set-CMBootImage.md)
