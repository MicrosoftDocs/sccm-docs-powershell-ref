---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: F0E16254-CBE7-4323-B877-2BBBA28E9E24
---

# Add-CMDriverToDriverPackage

## SYNOPSIS
Adds a device driver to a driver package.

## SYNTAX

### AddDriverToDriverPackageByObject_Object (Default)
```
Add-CMDriverToDriverPackage -Driver <IResultObject> -DriverPackage <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDriverToDriverPackageById_Name
```
Add-CMDriverToDriverPackage -DriverId <Int32> -DriverPackageName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDriverToDriverPackageById_Object
```
Add-CMDriverToDriverPackage -DriverId <Int32> -DriverPackage <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDriverToDriverPackageById_Id
```
Add-CMDriverToDriverPackage -DriverId <Int32> -DriverPackageId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDriverToDriverPackageByName_Id
```
Add-CMDriverToDriverPackage -DriverName <String> -DriverPackageId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDriverToDriverPackageByName_Name
```
Add-CMDriverToDriverPackage -DriverName <String> -DriverPackageName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDriverToDriverPackageByName_Object
```
Add-CMDriverToDriverPackage -DriverName <String> -DriverPackage <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDriverToDriverPackageByObject_Id
```
Add-CMDriverToDriverPackage -Driver <IResultObject> -DriverPackageId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDriverToDriverPackageByObject_Name
```
Add-CMDriverToDriverPackage -Driver <IResultObject> -DriverPackageName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDriverToDriverPackage** cmdlet adds a device driver to a driver package.
You can add Windows device drivers that have been imported into the driver catalog to an existing driver package.
When a device driver is added to a driver package, Microsoft System Center Configuration Manager copies the device driver content from the driver source location to the driver package.

## EXAMPLES

### Example 1: Add a driver to a driver package
```
PS C:\>Add-CMDriverToDriverPackage -DriverName "Adaptec Embedded SCSI HostRAID Controller" -DriverPackageName "DrvPkg01"
```

This command adds the driver named Adaptec Embedded SCSI HostRAID Controller to the driver package named DrvPkg01.

## PARAMETERS

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
Indicates that wildcard handling is disabled.

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
To obtain a **CMDriver** object, use the **Get-CMDriver** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddDriverToDriverPackageByObject_Object, AddDriverToDriverPackageByObject_Id, AddDriverToDriverPackageByObject_Name
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
Parameter Sets: AddDriverToDriverPackageById_Name, AddDriverToDriverPackageById_Object, AddDriverToDriverPackageById_Id
Aliases: 

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
Parameter Sets: AddDriverToDriverPackageByName_Id, AddDriverToDriverPackageByName_Name, AddDriverToDriverPackageByName_Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackage
Specifies a driver package object.
To obtain a **CMDriverPackage** object, use the **Get-CMDriverPackage** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddDriverToDriverPackageByObject_Object, AddDriverToDriverPackageById_Object, AddDriverToDriverPackageByName_Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DriverPackageId
Specifies the ID of a driver package.

```yaml
Type: String
Parameter Sets: AddDriverToDriverPackageById_Id, AddDriverToDriverPackageByName_Id, AddDriverToDriverPackageByObject_Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageName
Specifies the name of a driver package.

```yaml
Type: String
Parameter Sets: AddDriverToDriverPackageById_Name, AddDriverToDriverPackageByName_Name, AddDriverToDriverPackageByObject_Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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

[Remove-CMDriverFromDriverPackage](./Remove-CMDriverFromDriverPackage.md)

[Get-CMDriver](./Get-CMDriver.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)


