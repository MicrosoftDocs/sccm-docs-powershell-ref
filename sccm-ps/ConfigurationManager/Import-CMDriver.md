---
description: Import a device driver into the driver catalog.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: Import-CMDriver
---

# Import-CMDriver

## SYNOPSIS

Import a device driver into the driver catalog.

## SYNTAX

```
Import-CMDriver [-AdministrativeCategory <IResultObject[]>] [-AdministrativeCategoryName <String[]>]
 [-BootImagePackage <IResultObject[]>] [-DriverPackage <IResultObject[]>] [-EnableAndAllowInstall <Boolean>]
 [-ImportDuplicateDriverOption <ImportDuplicateDriverOption>] [-ImportFolder] -Path <String>
 [-SupportedPlatform <IResultObject[]>] [-SupportedPlatformName <String[]>]
 [-UpdateBootImageDistributionPoint <Boolean>] [-UpdateDriverPackageDistributionPoint <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Import-CMDriver** cmdlet imports one or more device drivers into the driver catalog in Configuration Manager.
When you import device drivers into the catalog, you can add the device drivers to driver packages or to boot image packages.

As part of the import process for the device driver, Configuration Manager reads the following information associated with the device:

- Provider
- Class
- Version
- Signature
- Supported hardware
- Supported platform

By default, the driver is named after the first hardware device that it supports. To rename the device driver, use the **-NewName** parameter of the [Set-CMDriver](Set-CMDriver.md) cmdlet.
The supported platforms list is based on the information in the INF file of the driver.
Because the accuracy of this information can vary, manually verify that the device driver is supported after you import it into the driver catalog.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import all device drivers in a path

This command imports all device drivers located in the network path `\\Server1\Driver`.

```powershell
Import-CMDriver -Path "\\Server1\Driver" -ImportFolder
```

### Example 2: Import a device driver by name

This command imports the driver named **driver.inf** from the network path `\\Server1\Driver`.

```powershell
Import-CMDriver -Path "\\Server1\Driver\driver.inf"
```

## PARAMETERS

### -AdministrativeCategory

Specify an array of category objects. To get this object, use the [Get-CMCategory](Get-CMCategory.md) cmdlet.

Assign the device drivers to a category for filtering purposes, such as Desktops or Notebooks.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AdministrativeCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeCategoryName

Instead of getting and specifying an object for a category with the **AdministrativeCategory** parameter, use this parameter to simply specify the name of a category. You can also use an array of category names.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AdministrativeCategoryNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImagePackage

Specify an array of boot image objects. To get this object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

Use this parameter to add the imported drivers to the specified boot images.

Only add drivers that Windows PE (WinPE) requires to boot:

- Make sure that the drivers that you add to the boot image match the architecture of the boot image.

- WinPE already comes with many drivers built-in. Add only network and storage drivers that aren't included in WinPE.

- Add only network and storage drivers to the boot image, unless there are requirements for other drivers in WinPE.

- It's best to use drivers that have a valid digital signature.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: BootImagePackages

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

### -DriverPackage

Specify an array of driver package objects. To get this object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

Use this parameter to add the imported drivers to the specified driver packages.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DriverPackages

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAndAllowInstall

Enable the driver and allow clients to install it during the [Auto Apply Driver](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_AutoApplyDrivers) task sequence step.

Drivers added to the driver package aren't affected.

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

### -ImportDuplicateDriverOption

Specify how Configuration Manager manages duplicate device drivers.

- `AppendCategory`: Import the driver and append a new category to the existing categories
`- KeepExistingCategory`: Import the driver and keep the existing categories
- `NotImport`: Don't import the driver
- `OverwriteCategory`: Import the driver and overwrite the existing categories

```yaml
Type: ImportDuplicateDriverOption
Parameter Sets: (All)
Aliases:
Accepted values: NotImport, AppendCategory, KeepExistingCategory, OverwriteCategory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFolder

Add this parameter to import all the device drivers in the target folder.

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

### -Path

Specify a path to the driver files to import.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UncFileLocation, Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportedPlatform

Specify a supported platform object to which the device driver is applicable and can run. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportedPlatformName

Specifies an array of supported platforms name on which the device driver can run. For example, `"All Windows 10 (64-bit)"`.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SupportedPlatformNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateBootImageDistributionPoint

Indicates whether Configuration Manager updates boot images on their distribution points to add the new drivers.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UpdateDistributionPointsForBootImagePackage, UpdateBootImageDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateDriverPackageDistributionPoint

If you use the **-DriverPackage** parameter, set this parameter to `$true` to update the driver package on assigned distribution points.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UpdateDistributionPointsforDriverPackage

Required: False
Position: Named
Default value: None
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

### IResultObject#SMS_Driver

## NOTES

## RELATED LINKS

[Get-CMDriver](Get-CMDriver.md)

[Set-CMDriver](Set-CMDriver.md)

[Enable-CMDriver](Enable-CMDriver.md)

[Disable-CMDriver](Disable-CMDriver.md)

[Remove-CMDriver](Remove-CMDriver.md)

[Get-CMCategory](Get-CMCategory.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers)
