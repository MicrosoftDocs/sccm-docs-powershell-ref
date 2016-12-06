---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834280
schema: 2.0.0
ms.assetid: 4EA61576-93BD-4095-9457-8D894A172115
---

# Update-CMAmtProvisioning

## SYNOPSIS
Updates provisioning for an Intel AMT-based computer.

## SYNTAX

### SearchByValueMandatory (Default)
```
Update-CMAmtProvisioning -Device <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Update-CMAmtProvisioning -DeviceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Update-CMAmtProvisioning -DeviceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Update-CMAMTProvisioning** cmdlet updates provisioning for an Intel Active Management Technology (Intel AMT)-based computer.
Provisioning is the process of initializing and registering a computer that has Intel AMT technology with Microsoft System Center Configuration Manager for out-of-band management.
This cmdlet updates provisioning information.

You can specify computers to update by using the System Center Configuration Manager device name or device ID, or you can use the [Get-CMDevice](./Get-CMDevice.md) cmdlet to get a device object.

## EXAMPLES

### Example 1: Update provisioning for a device by using an ID
```
PS C:\>Update-CMAmtProvisioning -DeviceID "16777230"
```

This command updates provisioning for an Intel AMT-based computer that has the device ID 16777230.

### Example 2: Update provisioning for a device by using an ID
```
PS C:\>Update-CMAmtProvisioning -DeviceName "Accn023.Contoso.com"
```

This command updates provisioning for an Intel AMT-based computer named Accn023.Contoso.com.

### Example 3: Enable audit logging by using a variable
```
PS C:\>$CMD = Get-CMDevice -Name "Accn023.Contoso.com"
PS C:\> Update-CMAmtProvisioning -Device $CMD
```

The first command gets a device object by using the **Get-CMDevice** cmdlet, and then stores it in the $CMD variable.

The second command updates provisioning for the device in $CMD.

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
Specifies a device object.
To obtain a device object, use **Get-CMDevice**.

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

### -DeviceId
Specifies an array of IDs of devices.

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
Specifies an array of names of devices.

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

[Invoke-CMAmtProvisioningDiscovery](./Invoke-CMAmtProvisioningDiscovery.md)

[Remove-CMAmtProvisioningData](./Remove-CMAmtProvisioningData.md)

[Get-CMDevice](./Get-CMDevice.md)
