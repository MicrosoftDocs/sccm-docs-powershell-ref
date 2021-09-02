---
description: Adds a driver to a boot image or removes a driver from a boot image.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMDriverBootImage
---

# Set-CMDriverBootImage

## SYNOPSIS
Adds a driver to a boot image or removes a driver from a boot image.

## SYNTAX

### SetDriverBootImagesById_Id (Default)
```
Set-CMDriverBootImage -BootImageId <String> -DriverId <Int32> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesById_Object
```
Set-CMDriverBootImage -BootImage <IResultObject> -DriverId <Int32> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesByName_Object
```
Set-CMDriverBootImage -BootImage <IResultObject> -DriverName <String> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesByObject_Object
```
Set-CMDriverBootImage -BootImage <IResultObject> -Driver <IResultObject> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesByName_Id
```
Set-CMDriverBootImage -BootImageId <String> -DriverName <String> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesByObject_Id
```
Set-CMDriverBootImage -BootImageId <String> -Driver <IResultObject> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesById_Name
```
Set-CMDriverBootImage -BootImageName <String> -DriverId <Int32> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesByName_Name
```
Set-CMDriverBootImage -BootImageName <String> -DriverName <String> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesByObject_Name
```
Set-CMDriverBootImage -BootImageName <String> -Driver <IResultObject> [-PassThru]
 -SetDriveBootImageAction <SetDriveBootImageActionType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDriverBootImage** cmdlet adds a driver to a boot image or removes a driver from a boot image.
You can add Windows device drivers that you have imported into the Configuration Manager driver catalog to one or more boot images.
You should add only mass storage device drivers and network adapter device drivers to boot images because other types of drivers are not needed and will increase the size of the boot image.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a driver to a boot image
```
PS XYZ:\> Set-CMDriverBootImage -SetDriveBootImageAction AddDriverToBootImage -DriverName "Adaptec Embedded SCSI HostRAID Controller" -BootImageName "Boot image (x64)"
```

This command adds the driver named Adaptec Embedded SCSI HostRAID Controller to the boot image named Boot image (x64).

### Example 2: Remove a driver from a boot image
```
PS XYZ:\> Set-CMDriverBootImage -SetDriveBootImageAction RemoveDriverFromBootImage -DriverName "Adaptec SCSI HostRAID Management Processor Device" -BootImageName "Boot image (x64)"
```

This command removes the driver named Adaptec SCSI HostRAID Management Processor Device from the boot image named Boot image (x64).

## PARAMETERS

### -BootImage
Specifies a **CMBootImage** object.
To obtain a **CMBootImage** object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetDriverBootImagesById_Object, SetDriverBootImagesByName_Object, SetDriverBootImagesByObject_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId
Specifies the ID of a boot image.

```yaml
Type: String
Parameter Sets: SetDriverBootImagesById_Id, SetDriverBootImagesByName_Id, SetDriverBootImagesByObject_Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageName
Specifies the name of a boot image.

```yaml
Type: String
Parameter Sets: SetDriverBootImagesById_Name, SetDriverBootImagesByName_Name, SetDriverBootImagesByObject_Name
Aliases:

Required: True
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

### -Driver
Specifies a driver object.
To obtain a **CMDriver** object, use the [Get-CMDriver](Get-CMDriver.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetDriverBootImagesByObject_Object, SetDriverBootImagesByObject_Id, SetDriverBootImagesByObject_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DriverId
Specifies the ID of a driver.

```yaml
Type: Int32
Parameter Sets: SetDriverBootImagesById_Id, SetDriverBootImagesById_Object, SetDriverBootImagesById_Name
Aliases: Id, CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverName
Specifies the name of a driver.

```yaml
Type: String
Parameter Sets: SetDriverBootImagesByName_Object, SetDriverBootImagesByName_Id, SetDriverBootImagesByName_Name
Aliases:

Required: True
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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -SetDriveBootImageAction
Specifies the boot image action.
The acceptable values for this parameter are:

- AddDriverToBootImage
- RemoveDriverFromBootImage

```yaml
Type: SetDriveBootImageActionType
Parameter Sets: (All)
Aliases:
Accepted values: AddDriverToBootImage, RemoveDriverFromBootImage

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDriver](Get-CMDriver.md)
