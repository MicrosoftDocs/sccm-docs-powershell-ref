---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834105
schema: 2.0.0
ms.assetid: C8BFF87E-662F-486D-9F4A-27428FD4DC7A
---

# Invoke-CMClientNotification

## SYNOPSIS
Sends a notification to client computers to trigger an immediate client action.

## SYNTAX

### SearchByDeviceValueMandatory (Default)
```
Invoke-CMClientNotification -Device <IResultObject> -NotificationType <ClientNotificationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Invoke-CMClientNotification -DeviceName <String> -NotificationType <ClientNotificationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Invoke-CMClientNotification -DeviceId <String> -NotificationType <ClientNotificationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMClientNotification -DeviceCollectionName <String> -NotificationType <ClientNotificationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMClientNotification -DeviceCollectionId <String> -NotificationType <ClientNotificationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMClientNotification -DeviceCollection <IResultObject> -NotificationType <ClientNotificationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMClientNotification** cmdlet sends a notification to client computers to trigger an immediate client action.
You can specify one or more client computers, or send a notification to all the computers in a specified device collection.

## EXAMPLES

### Example 1: Send a notification to trigger an event
```
PS C:\>Invoke-CMClientNotification -DeviceName "Computer073" -NotificationType RequestMachinePolicyNow
```

This command sends a notification of the type RequestMachinePolicyNow to the device named Computer073.

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
Specifies a **CMDevice** object.
To obtain a **CMDevice** object, use the [Get-CMDevice](./Get-CMDevice.md) cmdlet.

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
Specifies a **CMDeviceCollection** object.
To obtain a **CMDeviceCollection** object, use the [Get-CMDeviceCollection](./Get-CMDeviceCollection.md) cmdlet.

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
Specifies a device name.
You can specify a NetBIOS name or a fully qualified domain name (FQDN).

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

### -NotificationType
Specifies the type of notification to send.
Valid values are: 

- RequestMachinePolicyNow.
The client computer requests the latest machine policy from the management point.
Machine policy includes configuration settings for a computer, or software updates that are deployed to a computer.
- RequestUsersPolicyNow.
The client computer requests the latest user policy from the management point.
User policy includes applications or packages deployed for a user.

```yaml
Type: ClientNotificationType
Parameter Sets: (All)
Aliases: 
Accepted values: RequestMachinePolicyNow, RequestUsersPolicyNow
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

[Get-CMDevice](./Get-CMDevice.md)

[Get-CMDeviceCollection](./Get-CMDeviceCollection.md)


