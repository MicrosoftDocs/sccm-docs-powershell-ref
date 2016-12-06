---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833764
schema: 2.0.0
ms.assetid: 6299CEF1-998E-49EA-A49A-2F2AA2FE13A4
---

# Add-CMUserAffinityToDevice

## SYNOPSIS
Adds a primary user to one or more devices in the Configuration Manager hierarchy.

## SYNTAX

### AddUserAffinityByDeviceName (Default)
```
Add-CMUserAffinityToDevice -DeviceName <String[]> [-UserId <String>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddUserAffinityByDeviceId
```
Add-CMUserAffinityToDevice -DeviceId <String[]> [-UserId <String>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMUserAffinityToDevice** cmdlet associates the devices with a primary user in Microsoft System Center Configuration Manager.
You can specify the devices to associate with the primary user by their names or IDs.
You can specify the primary user by their name or ID.

User device affinity is a method of associating a user with one or more specified devices.
This allows you to deploy applications to a user without the requirement to know the name of all the user's devices.
Instead of deploying the application to all the devices of a user, you deploy the application to the user and the application automatically installs on all devices that are associated with that user.

## EXAMPLES

### Example 1: Add a primary user to a device
```
PS C:\>Add-CMUserAffinityToDevice -DeviceName "CMCEN-DIST-02" -UserId "2063597981"
```

This command adds the primary user that has the ID 2063597981 to the device named CMCEN-DIST-02.

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

### -DeviceId
Specifies an array of IDs of the devices that you want to associate with the primary user.

```yaml
Type: String[]
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

### -UserId
Specifies the ID of a user.

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

### -UserName
Specifies the name of the primary user.

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

[Remove-CMUserAffinityFromDevice](./Remove-CMUserAffinityFromDevice.md)


