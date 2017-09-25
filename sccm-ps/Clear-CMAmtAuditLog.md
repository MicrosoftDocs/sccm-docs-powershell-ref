---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833831
schema: 2.0.0
ms.assetid: 4AF1703D-DBDE-40D7-AEBB-DA96D2BEF98D
---

# Clear-CMAmtAuditLog

## SYNOPSIS
Clears audit log entries for Intel AMT-based computers.

## SYNTAX

### SearchByValueMandatory (Default)
```
Clear-CMAmtAuditLog -Device <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Clear-CMAmtAuditLog -DeviceName <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Clear-CMAmtAuditLog -DeviceId <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByCollectionValueMandatory
```
Clear-CMAmtAuditLog -DeviceCollection <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByCollectionIdMandatory
```
Clear-CMAmtAuditLog -DeviceCollectionId <String[]> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByCollectionNameMandatory
```
Clear-CMAmtAuditLog -DeviceCollectionName <String[]> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Clear-CMAmtAuditLog** cmdlet clears audit log entries for Intel Active Management Technology (Intel AMT)-based computers.
The audit log records authorized and authenticated out-of-band management activities performed on Intel AMT computers.

Depending on your Intel AMT version, when the audit log becomes 85 percent full, noncritical log entries might not be written to the log or might overwrite old entries.
This cmdlet does not stop audit logging.
You can use the Disable-CMAmtAuditLog cmdlet to stop logging.

You can specify computers by using the Microsoft System Center Configuration Manager device name or device ID, or you can use the [Get-CMDevice](./Get-CMDevice.md) cmdlet to get a device object.
You can also clear audit logs for all the devices in a System Center Configuration Manager collection.
Specify a collection by using the collection name or collection ID, or you can use the [Get-CMDeviceCollection](./Get-CMDeviceCollection.md) cmdlet to get a device collection object.

## EXAMPLES

### Example 1: Clear the audit log by using an ID
```
PS C:\>Clear-CMAmtAuditLog -DeviceID "16777230"
```

This command clears the Intel AMT audit log for a device that has the ID 16777230.

### Example 2: Clear audit logs for a device collection
```
PS C:\>Clear-CMAmtAuditLog -DeviceCollectionName "Floor03"
```

This command clears Intel AMT audit logs for the devices in a collection named Floor03.

### Example 3: Clear the audit log by using a variable
```
PS C:\> $CMD = Get-CMDevice -Name "Accn023.Contoso.com" 
PS C:\> Clear-CMAmtAuditLog -Device $CMD -Force
```

The first command gets a device object by using the **Get-CMDevice** cmdlet, and then stores it in the $CMD variable.

The second command clears the Intel AMT audit for the device in $CMD.
The command uses the *Force* parameter.
Therefore, the command does not prompt you for confirmation.

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
Aliases: InputObject
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceCollection
Specifies a device collection object.
To obtain a device collection object, use **Get-CMDeviceCollection**.

```yaml
Type: IResultObject
Parameter Sets: SearchByCollectionValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceCollectionId
Specifies an array of IDs of device collections.

```yaml
Type: String[]
Parameter Sets: SearchByCollectionIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceCollectionName
Specifies an array of names of device collections.

```yaml
Type: String[]
Parameter Sets: SearchByCollectionNameMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

[Disable-CMAmtAuditLog](./Disable-CMAmtAuditLog.md)

[Enable-CMAmtAuditLog](./Enable-CMAmtAuditLog.md)

[Get-CMDevice](./Get-CMDevice.md)

[Get-CMDeviceCollection](./Get-CMDeviceCollection.md)


