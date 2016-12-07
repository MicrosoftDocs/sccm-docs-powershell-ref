---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834097
schema: 2.0.0
ms.assetid: 90208E20-E077-40AB-A50F-B7113BA07775
---

# Invoke-CMAmtProvisioningDiscovery

## SYNOPSIS
Checks whether computers have Intel AMT hardware.

## SYNTAX

### SearchByDeviceValueMandatory (Default)
```
Invoke-CMAmtProvisioningDiscovery -Device <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Invoke-CMAmtProvisioningDiscovery -DeviceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Invoke-CMAmtProvisioningDiscovery -DeviceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMAmtProvisioningDiscovery -DeviceCollectionName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMAmtProvisioningDiscovery -DeviceCollectionId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMAmtProvisioningDiscovery -DeviceCollection <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMAmtProvisioningDiscovery** cmdlet checks whether computers have Intel Active Management Technology (Intel AMT) hardware that supports out-of-band management.
You can check individual computers or computers that belong to a Microsoft System Center Configuration Manager collection.

## EXAMPLES

### Example 1: Check a computer for Intel AMT hardware by using an ID
```
PS C:\>Invoke-CMAmtProvisioningDiscovery -DeviceID "16777230"
```

This command checks for Intel AMT-based hardware on a device that has the ID 16777230.

### Example 2: Check computers for Intel AMT hardware in a named device collection
```
PS C:\>Invoke-CMAmtProvisioningDiscovery -DeviceCollectionName "Floor03"
```

This command checks for Intel AMT-based hardware on the devices that belong to the collection named Floor03.

### Example 3: Check for a computer for Intel AMT hardware by using a variable
```
PS C:\>$CMD = Get-CMDevice -Name "Accn023.Contoso.com"
PS C:\> Invoke-CMAmtProvisioningDiscovery -Device $CMD
```

The first command gets a device object by using the **Get-CMDevice** command, and then stores it in the $CMD variable.

The second command checks for Intel AMT-based technology on the device stored in the $CMD variable.

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

### -Device
Specifies a device object in Configuration Manager.
To obtain a device object, use the [Get-CMDevice](./Get-CMDevice.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByDeviceValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceCollection
Specifies a device collection object in Configuration Manager.
To obtain a device collection object, use the [Get-CMDeviceCollection](./Get-CMDeviceCollection.md) cmdlet.

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

### -DeviceCollectionId
Specifies the ID of a device collection.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceCollectionName
Specifies the name of a device collection.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceId
Specifies the ID of a device.

```yaml
Type: String
Parameter Sets: SearchByDeviceIdMandatory
Aliases: ResourceID
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
Parameter Sets: SearchByDeviceNameMandatory
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

[Update-CMAMTProvisioning](./Update-CMAMTProvisioning.md)

[Remove-CMAmtProvisioningData](./Remove-CMAmtProvisioningData.md)

[Get-CMDevice](./Get-CMDevice.md)

[Get-CMDeviceCollection](./Get-CMDeviceCollection.md)


