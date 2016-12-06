---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833801
schema: 2.0.0
ms.assetid: A42E8F2E-F74F-4D26-9A13-761446253F83
---

# Set-CMDeviceOwnership

## SYNOPSIS
Configures ownership type for a device.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMDeviceOwnership -InputObject <IResultObject> -OwnershipType <DeviceOwnershipType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMDeviceOwnership -DeviceName <String> -OwnershipType <DeviceOwnershipType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMDeviceOwnership -DeviceId <String> -OwnershipType <DeviceOwnershipType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDeviceOwnership** cmdlet configures ownership type for a modern device.
For a personal device, the information gathered is limited, and personal information is not removed during a wipe operation.
For a company-owned device, additional information can be gathered and deleted during a wipe operation.

## EXAMPLES

### Example 1: Identify a device as a company asset
```
PS C:\>Set-CMDeviceOwnership -DeviceId "209846738" -OwnershipType Company
```

This command identifies the specified device as a company asset.

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
Specifies an array of device IDs.

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
Specifies an array of device names.

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
Specifies a **CMDevice** object.
To obtain a **CMDevice** object, use the [Get-CMDevice](./Get-CMDevice.md) cmdlet.

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

### -OwnershipType
Specifies the type of ownership for a device.
The acceptable values for this parameter are:

- Company.
The device is a company asset.
- Personal.
The device is not a company asset.

```yaml
Type: DeviceOwnershipType
Parameter Sets: (All)
Aliases: 
Accepted values: Company, Personal

Required: True
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

[Invoke-CMDeviceWipe](./Invoke-CMDeviceWipe.md)

[Get-CMDevice](./Get-CMDevice.md)


