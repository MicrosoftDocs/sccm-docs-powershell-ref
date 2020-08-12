---
description: Removes a driver from a driver package.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMDriverFromDriverPackage
---

# Remove-CMDriverFromDriverPackage

## SYNOPSIS
Removes a driver from a driver package.

## SYNTAX

### RemoveDriverFromDriverPackageById_Id (Default)
```
Remove-CMDriverFromDriverPackage [-Force] -DriverId <Int32> -DriverPackageId <String>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageById_Name
```
Remove-CMDriverFromDriverPackage [-Force] -DriverId <Int32> -DriverPackageName <String>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageById_Object
```
Remove-CMDriverFromDriverPackage [-Force] -DriverId <Int32> -DriverPackage <IResultObject>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Id
```
Remove-CMDriverFromDriverPackage [-Force] -DriverName <String> -DriverPackageId <String>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Name
```
Remove-CMDriverFromDriverPackage [-Force] -DriverName <String> -DriverPackageName <String>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Object
```
Remove-CMDriverFromDriverPackage [-Force] -DriverName <String> -DriverPackage <IResultObject>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Id
```
Remove-CMDriverFromDriverPackage [-Force] -Driver <IResultObject> -DriverPackageId <String>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Name
```
Remove-CMDriverFromDriverPackage [-Force] -Driver <IResultObject> -DriverPackageName <String>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Object
```
Remove-CMDriverFromDriverPackage [-Force] -Driver <IResultObject> -DriverPackage <IResultObject>
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDriverFromDriverPackage** cmdlet removes a driver from a driver package in Configuration Manager.
When you remove a driver from a driver package, the device driver content is deleted from the source directory share for the driver package.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove a driver from a driver package
```
PS XYZ:\> Remove-CMDriverfromDriverPackage -DriverName "Adaptec Embedded SCSI HostRAID Controller" -DriverPackageName "DrvPkg01"
```

This command removes the driver named Adaptec Embedded SCSI HostRAID Controller from the boot image named DrvPkg01.

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

### -Driver
Specifies a driver object.
To obtain a **CMDriver** object, use the [Get-CMDriver](Get-CMDriver.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveDriverFromDriverPackageByObject_Id, RemoveDriverFromDriverPackageByObject_Name, RemoveDriverFromDriverPackageByObject_Object
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
Parameter Sets: RemoveDriverFromDriverPackageById_Id, RemoveDriverFromDriverPackageById_Name, RemoveDriverFromDriverPackageById_Object
Aliases: CIId, Id, CI_ID

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
Parameter Sets: RemoveDriverFromDriverPackageByName_Id, RemoveDriverFromDriverPackageByName_Name, RemoveDriverFromDriverPackageByName_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackage
Specifies a **CMDriverPackage** object.
To obtain a **CMDriverPackage** object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveDriverFromDriverPackageById_Object, RemoveDriverFromDriverPackageByName_Object, RemoveDriverFromDriverPackageByObject_Object
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
Parameter Sets: RemoveDriverFromDriverPackageById_Id, RemoveDriverFromDriverPackageByName_Id, RemoveDriverFromDriverPackageByObject_Id
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
Parameter Sets: RemoveDriverFromDriverPackageById_Name, RemoveDriverFromDriverPackageByName_Name, RemoveDriverFromDriverPackageByObject_Name
Aliases:

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

### -UpdateDistributionPoints
{{ Fill UpdateDistributionPoints Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UpdateDistributionPoint, UpdateDistributionPointForDriverPackage, UpdateDistributionPointsForDriverPackage

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMDriverToDriverPackage](Add-CMDriverToDriverPackage.md)

[Get-CMDriver](Get-CMDriver.md)


