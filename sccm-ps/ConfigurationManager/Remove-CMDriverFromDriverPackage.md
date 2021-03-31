---
description: Removes a driver from a driver package.
external help file: AdminUI.PS.dll-Help.xml
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
Remove-CMDriverFromDriverPackage -DriverId <Int32> -DriverPackageId <String> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Id
```
Remove-CMDriverFromDriverPackage -Driver <IResultObject> -DriverPackageId <String> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Name
```
Remove-CMDriverFromDriverPackage -Driver <IResultObject> -DriverPackageName <String> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Object
```
Remove-CMDriverFromDriverPackage -Driver <IResultObject> -DriverPackage <IResultObject> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageById_Name
```
Remove-CMDriverFromDriverPackage -DriverId <Int32> -DriverPackageName <String> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageById_Object
```
Remove-CMDriverFromDriverPackage -DriverId <Int32> -DriverPackage <IResultObject> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Id
```
Remove-CMDriverFromDriverPackage -DriverName <String> -DriverPackageId <String> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Name
```
Remove-CMDriverFromDriverPackage -DriverName <String> -DriverPackageName <String> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Object
```
Remove-CMDriverFromDriverPackage -DriverName <String> -DriverPackage <IResultObject> [-Force]
 [-UpdateDistributionPoints <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDriverFromDriverPackage** cmdlet removes a driver from a driver package in Configuration Manager.
When you remove a driver from a driver package, the device driver content is deleted from the source directory share for the driver package.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a driver from a driver package
```
PS XYZ:\> Remove-CMDriverfromDriverPackage -DriverName "Adaptec Embedded SCSI HostRAID Controller" -DriverPackageName "DrvPkg01"
```

This command removes the driver named Adaptec Embedded SCSI HostRAID Controller from the boot image named DrvPkg01.

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
Parameter Sets: RemoveDriverFromDriverPackageByObject_Object, RemoveDriverFromDriverPackageById_Object, RemoveDriverFromDriverPackageByName_Object
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
Parameter Sets: RemoveDriverFromDriverPackageById_Id, RemoveDriverFromDriverPackageByObject_Id, RemoveDriverFromDriverPackageByName_Id
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
Parameter Sets: RemoveDriverFromDriverPackageByObject_Name, RemoveDriverFromDriverPackageById_Name, RemoveDriverFromDriverPackageByName_Name
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

[Add-CMDriverToDriverPackage](Add-CMDriverToDriverPackage.md)

[Get-CMDriver](Get-CMDriver.md)


