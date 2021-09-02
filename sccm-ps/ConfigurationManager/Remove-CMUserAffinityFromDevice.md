---
description: Removes a primary user from one or more devices in the Configuration Manager hierarchy.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMUserAffinityFromDevice
---

# Remove-CMUserAffinityFromDevice

## SYNOPSIS
Removes a primary user from one or more devices in the Configuration Manager hierarchy.

## SYNTAX

### RemoveUserAffinityByDeviceName (Default)
```
Remove-CMUserAffinityFromDevice -DeviceName <String[]> [-Force] [-UserId <Int32[]>] [-UserName <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveUserAffinityByDeviceId
```
Remove-CMUserAffinityFromDevice -DeviceId <Int32[]> [-Force] [-UserId <Int32[]>] [-UserName <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMUserAffinityFromDevice** cmdlet removes a primary user from the devices.

User device affinity is a method of associating a user with one or more specified devices in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a primary user from a device
```
PS XYZ:\> Remove-CMUserAffinityFromDevice -DeviceId "209846738" -UserId "206359374"
```

This command removes the association between the user that has the ID 206359374 and the device that has the ID 209846738.

## PARAMETERS

### -DeviceId
Specifies an array of IDs of the devices.

```yaml
Type: Int32[]
Parameter Sets: RemoveUserAffinityByDeviceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of names of the devices.

```yaml
Type: String[]
Parameter Sets: RemoveUserAffinityByDeviceName
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
Specifies the name of the primary user that you want to disassociate from the specified devices.

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

[Add-CMUserAffinityToDevice](Add-CMUserAffinityToDevice.md)


