---
title: Set-CMDriver
titleSuffix: Configuration Manager
description: Changes the settings of a device driver.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Set-CMDriver

## SYNOPSIS
Changes the settings of a device driver.

## SYNTAX

### SetDriverByResultObject (Default)
```
Set-CMDriver -InputObject <IResultObject> [-NewName <String>] [-Description <String>] [-DriverSource <String>]
 [-EnableAndAllowInstall <Boolean>] [-AdministrativeCategory <IResultObject[]>]
 [-AddAdministrativeCategory <IResultObject[]>] [-RemoveAdministrativeCategory <IResultObject[]>]
 [-ClearAdministrativeCategory] [-RunOnAnyPlatform] [-SupportedPlatformName <String[]>]
 [-AddDriverPackage <IResultObject[]>] [-RemoveDriverPackage <IResultObject[]>]
 [-UpdateDriverDistributionPoint <Boolean>] [-AddBootImagePackage <IResultObject[]>]
 [-RemoveBootImagePackage <IResultObject[]>] [-UpdateBootImageDistributionPoint <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverByName
```
Set-CMDriver -Name <String> [-NewName <String>] [-Description <String>] [-DriverSource <String>]
 [-EnableAndAllowInstall <Boolean>] [-AdministrativeCategory <IResultObject[]>]
 [-AddAdministrativeCategory <IResultObject[]>] [-RemoveAdministrativeCategory <IResultObject[]>]
 [-ClearAdministrativeCategory] [-RunOnAnyPlatform] [-SupportedPlatformName <String[]>]
 [-AddDriverPackage <IResultObject[]>] [-RemoveDriverPackage <IResultObject[]>]
 [-UpdateDriverDistributionPoint <Boolean>] [-AddBootImagePackage <IResultObject[]>]
 [-RemoveBootImagePackage <IResultObject[]>] [-UpdateBootImageDistributionPoint <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverById
```
Set-CMDriver -Id <String> [-NewName <String>] [-Description <String>] [-DriverSource <String>]
 [-EnableAndAllowInstall <Boolean>] [-AdministrativeCategory <IResultObject[]>]
 [-AddAdministrativeCategory <IResultObject[]>] [-RemoveAdministrativeCategory <IResultObject[]>]
 [-ClearAdministrativeCategory] [-RunOnAnyPlatform] [-SupportedPlatformName <String[]>]
 [-AddDriverPackage <IResultObject[]>] [-RemoveDriverPackage <IResultObject[]>]
 [-UpdateDriverDistributionPoint <Boolean>] [-AddBootImagePackage <IResultObject[]>]
 [-RemoveBootImagePackage <IResultObject[]>] [-UpdateBootImageDistributionPoint <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDriver** cmdlet changes settings of a device driver in the driver catalog.

## EXAMPLES

### Example 1: Modify a driver
```
PS C:\> $Driver = Get-CMDriver -Name "cdrom.sys"
PS C:\> Set-CMDriver -InputObject $Driver -NewName "testDriver" -Description "Test configuration" -EnableAndAllowInstall $True -RunOnAnyPlatform $True
```

The first command gets a device driver named cdrom.sys by using the [Get-CMDriver](Get-CMDriver.md) cmdlet.
The command stores that object in the $Driver variable.

The second command renames the driver and adds a description.
The command specifies values for the *EnableAndAllowInstall* and *RunOnAnyPlatform* parameters.

### Example 2: Modify a driver by using the pipeline
```
PS C:\> Get-CMDriver -Name "cdrom.sys" | Set-CMDriver -NewName testDriver -Description description -EnableAndAllowInstall $True -RunOnAnyPlatform $True
```

This command gets a driver named cdrom.sys, and then passes it to the current cmdlet by using the pipeline operator.
The current cmdlet renames the driver and adds a description.
The command specifies values for *EnableAndAllowInstall* and *RunOnAnyPlatform*.

## PARAMETERS

### -AddAdministrativeCategory
Specifies an array of administrative category objects that this cmdlet adds to a driver.
To obtain an administrative category object, use the [Get-CMCategory](Get-CMCategory.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddAdministrativeCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddBootImagePackage
Specifies an array of boot image objects.
Use this parameter to specify the boot images that can install the device drivers.
To obtain a boot image object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddDriverPackage
Specifies an array of driver package objects.
Use this parameter to specify the driver packages that Configuration Manager uses to distribute the device drivers.
To obtain a driver package object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeCategory
Specifies an array of administrative categories.
Assign the device drivers to an administrative category for filtering purposes, such as Desktops or Notebooks categories.

To obtain an administrative category object, use the **Get-CMCategory** cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearAdministrativeCategory
Indicates that this cmdlet removes all the administrative category objects from the driver.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearAdministrativeCategories

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

### -Description
Specifies a description for the device driver.

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

### -DriverSource
Specifies the driver package source location.
When you create a driver package, the source location of the package must point to an empty network share that is not used by another driver package.

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

### -EnableAndAllowInstall
Indicates whether Configuration Manager enables the drivers and allows computers to install the drivers.

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

### -Id
Specifies the ID of a device driver.

```yaml
Type: String
Parameter Sets: SetDriverById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a driver object.
To obtain a driver object, use the **Get-CMDriver** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetDriverByResultObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a device driver.

```yaml
Type: String
Parameter Sets: SetDriverByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the device driver.

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

### -PassThru
Returns an object that represents the driver.
By default, this cmdlet does not generate any output.

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

### -RemoveAdministrativeCategory
Specifies an array of administrative category objects that this cmdlet removes from a driver.
To obtain an administrative category object, use **Get-CMCategory**.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveAdministrativeCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveBootImagePackage
Specifies an array of boot image objects.
Use this parameter to remove the boot images that can install the device driver.
To obtain a boot image object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveDriverPackage
Specifies an array of driver package objects.
Use this parameter to remove the driver packages that Configuration Manager uses to distribute the device drivers.
To obtain a driver package object, use the **Get-CMDriverPackage** cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunOnAnyPlatform
Indicates that the device driver can run on all platforms.

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

### -SupportedPlatformName
Specifies an array of names of platforms on which the device driver can run.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

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

### -UpdateDriverDistributionPoint
Indicates that Configuration Manager updates distribution points when the device driver is added to the driver package.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UpdateDistributionPointsForDriverPackage, UpdateDriverDistributionPoints

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

[Disable-CMDriver](Disable-CMDriver.md)

[Enable-CMDriver](Enable-CMDriver.md)

[Get-CMDriver](Get-CMDriver.md)

[Import-CMDriver](Import-CMDriver.md)

[Remove-CMDriver](Remove-CMDriver.md)

[Get-CMCategory](Get-CMCategory.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)
