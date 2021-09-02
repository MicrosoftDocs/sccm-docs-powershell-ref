---
description: Adds a primary user to one or more devices in the Configuration Manager hierarchy.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMUserAffinityToDevice
---

# Add-CMUserAffinityToDevice

## SYNOPSIS
Adds a primary user to one or more devices in the Configuration Manager hierarchy.

## SYNTAX

### AddUserAffinityByDeviceName (Default)
```
Add-CMUserAffinityToDevice -DeviceName <String[]> [-UserId <Int32[]>] [-UserName <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddUserAffinityByDeviceId
```
Add-CMUserAffinityToDevice -DeviceId <Int32[]> [-UserId <Int32[]>] [-UserName <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMUserAffinityToDevice** cmdlet associates the devices with a primary user in Configuration Manager.
You can specify the devices to associate with the primary user by their names or IDs.
You can specify the primary user by their name or ID.

User device affinity is a method of associating a user with one or more specified devices.
This allows you to deploy applications to a user without the requirement to know the name of all the user's devices.
Instead of deploying the application to all the devices of a user, you deploy the application to the user and the application automatically installs on all devices that are associated with that user.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a primary user to a device
```
PS XYZ:\>Add-CMUserAffinityToDevice -DeviceName "CMCEN-DIST-02" -UserId "2063597981"
```

This command adds the primary user that has the ID 2063597981 to the device named CMCEN-DIST-02.

## PARAMETERS

### -DeviceId
Specifies an array of IDs of the devices that you want to associate with the primary user.

```yaml
Type: Int32[]
Parameter Sets: AddUserAffinityByDeviceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of names of the devices that you want to associate with the primary user.

```yaml
Type: String[]
Parameter Sets: AddUserAffinityByDeviceName
Aliases: ResourceName

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

### -UserId
Specifies the ID of a user.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: UserIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the name of the primary user.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: UserNames

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

### System.Object
## NOTES

## RELATED LINKS

[Remove-CMUserAffinityFromDevice](Remove-CMUserAffinityFromDevice.md)


