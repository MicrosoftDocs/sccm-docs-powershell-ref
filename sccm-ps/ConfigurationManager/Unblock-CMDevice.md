---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: F51FCE47-CF79-4C56-8DBD-40F98BAF4370
online version: https://go.microsoft.com/fwlink/?linkid=834268
schema: 2.0.0
---

# Unblock-CMDevice

## SYNOPSIS
Unblocks a client device.

## SYNTAX

### SearchByValueMandatory (Default)
```
Unblock-CMDevice [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Unblock-CMDevice -DeviceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Unblock-CMDevice -DeviceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Unblock-CMDevice** cmdlet unblocks one or more Microsoft System Center Configuration Manager client devices.
You must unblock a device from the client's assigned site.
You cannot unblock the device from sites higher in the hierarchy.

## EXAMPLES

### Example 1: Unblock a device
```
PS C:\>Unbock-CMDevice -DeviceName "Test-DIST02"
```

This command unblocks the device named Test-DIST02.

### Example 2: Get a device and unblock it
```
PS C:\> Get-CMDevice -Name "WIN10-86-33" | Unblock-CMDevice
```

This command gets the device object named WIN10-86-33 and uses the pipeline operator to pass the object to **Unblock-CMDevice**, which unblocks the device object.

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
Specifies the ID of a device.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies the name of the device.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name

Required: True
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
To obtain a device object, use the [Get-CMDevice](Get-CMDevice.md) cmdlet.

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

[Approve-CMDevice](Approve-CMDevice.md)

[Block-CMDevice](Block-CMDevice.md)

[Get-CMDevice](Get-CMDevice.md)

[Remove-CMDevice](Remove-CMDevice.md)
