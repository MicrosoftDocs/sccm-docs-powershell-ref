---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833812
schema: 2.0.0
ms.assetid: D6A79C88-CE68-45E7-88B3-43F94F73DDE9
---

# Approve-CMDevice

## SYNOPSIS
Approves a device.

## SYNTAX

### SearchByValueMandatory (Default)
```
Approve-CMDevice -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Approve-CMDevice -DeviceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Approve-CMDevice -DeviceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Approve-CMDevice** cmdlet approves one or more Microsoft System Center Configuration Manager device clients to join a site.
You cannot approve a Configuration Manager client until you have installed the device and assigned it to a site.

## EXAMPLES

### Example 1: Approve a device
```
PS C:\>Approve-CMDevice -DeviceName "TestVlan-site2"
```

This command approves the device named TestVlan-site2.

### Example 2: Get a device and approve it
```
PS C:\>Get-CMDevice -Name "TestVlan-site2" | Approve-CMDevice
```

This command gets the device object named TestVlan-site2 and uses the pipeline operator to pass the object to **Approve-CMDevice**, which approves the device object.

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
Specifies the name of a device.

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

### -InputObject
Specifies a device object.
To obtain a device object, use the [Get-CMDevice](./Get-CMDevice.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 
Required: True
Position: Named
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

[Block-CMDevice](./Block-CMDevice.md)

[Get-CMDevice](./Get-CMDevice.md)

[Remove-CMDevice](./Remove-CMDevice.md)

[Unblock-CMDevice](./Unblock-CMDevice.md)


