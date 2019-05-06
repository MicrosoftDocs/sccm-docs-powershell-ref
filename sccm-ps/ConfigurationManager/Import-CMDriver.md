---
title: Import-CMDriver
titleSuffix: Configuration Manager
description: Imports a device driver into Configuration Manager.
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Import-CMDriver

## SYNOPSIS
Imports a device driver into Configuration Manager.

## SYNTAX

```
Import-CMDriver -Path <String> [-ImportFolder] [-ImportDuplicateDriverOption <ImportDuplicateDriverOption>]
 [-EnableAndAllowInstall <Boolean>] [-AdministrativeCategory <IResultObject[]>]
 [-SupportedPlatformName <String[]>] [-SupportedPlatform <IResultObject[]>] [-DriverPackage <IResultObject[]>]
 [-UpdateDriverPackageDistributionPoint <Boolean>] [-BootImagePackage <IResultObject[]>]
 [-UpdateBootImageDistributionPoint <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMDriver** cmdlet imports one or more device drivers into the driver catalog in Microsoft System Center Configuration Manager.
When you import device drivers into the catalog, you can add the device drivers to driver packages or to boot image packages.

As part of the import process for the device driver, Configuration Manager reads the provider, class, version, signature, supported hardware, and supported platform information that is associated with the device.
By default, the driver is named after the first hardware device that it supports; however, you can rename the device driver later.
The supported platforms list is based on the information in the INF file of the driver.
Because the accuracy of this information can vary, manually verify that the device driver is supported after it is imported into the driver catalog.

## EXAMPLES

### Example 1: Import all device drivers in a path
```
PS C:\>Import-CMDriver -UncFileLocation "\\Server1\Driver" -ImportFolder
```

This command imports all device drivers located in the network path \\\\Server1\Driver.

### Example 2: Import a device driver by name
```
PS C:\>Import-CMDriver -UncFileLocation "\\Server1\Driver\driver.inf"
```

This command imports the driver named driver.inf from the network path \\\\Server1\Driver.

## PARAMETERS

### -AdministrativeCategory
Specifies an array of administrative categories.
To obtain an administrative category object, use the Get-CMCategory cmdlet.

Assign the device drivers to an administrative category for filtering purposes, such as Desktops or Notebooks categories.

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

### -BootImagePackage
Specifies an array of boot image objects.
To obtain a boot image object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

Use this parameter to specify the boot images that can install the imported device drivers.

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

### -DriverPackage
Specifies an array of driver package objects.
To obtain a driver package object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

Use this parameter to specify the driver packages that Configuration Manager uses to distribute the device drivers.

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
Indicates whether Configuration Manager enables computers to install the device drivers used with the Auto Apply Driver task sequence step.
Drivers added to the driver package are not affected.

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

### -ImportDuplicateDriverOption
Specifies how Configuration Manager manages duplicate device drivers.
Valid values are:

- AppendCategory
- KeepExistingCategory
- NotImport
- OverwriteCategory

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
Indicates that Configuration Manager imports all the device drivers in the import folder.

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
Specifies a platform object on which the device driver can run.

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
Specifies an array of names of platforms on which the device driver can run.

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
Indicates whether Configuration Manager adds the drivers to packages and deploys them to distribution points so that computers can use them.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

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


