---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: 16B5581F-4F33-4117-AED7-546E20A281C3
online version: https://go.microsoft.com/fwlink/?linkid=834037
schema: 2.0.0
---

# Remove-CMDevice

## SYNOPSIS
Removes a client device from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMDevice [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMDevice [-Name] <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMDevice [-ResourceId] <Int32> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDevice** cmdlet removes one or more Microsoft System Center Configuration Manager client devices.
Do not remove a client if you want to uninstall the client or remove it from a collection.

## EXAMPLES

### Example 1: Remove a device by name
```
PS C:\> Remove-CMDevice -DeviceName "WIN10-86-33"
```

This command removes the device named WIN10-86-33.

### Example 2: Get a device and remove it
```
PS C:\> Get-CMDevice -Name "TestVLAN-VNEXT" | Remove-CMDevice
```

This command gets the device object named TestVLAN-VNEXT and uses the pipeline operator to pass the object to **Remove-CMDevice**, which removes the device object.

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

### -InputObject
Specifies a device object.
To obtain a device object, use the [Get-CMDevice](./Get-CMDevice.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a device.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: DeviceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifies the resource ID of a device.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: Id, DeviceId

Required: True
Position: 0
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

[Approve-CMDevice](./Approve-CMDevice.md)

[Block-CMDevice](./Block-CMDevice.md)

[Get-CMDevice](./Get-CMDevice.md)

[Unblock-CMDevice](./Unblock-CMDevice.md)


