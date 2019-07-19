<<<<<<< HEAD
---
title: New-CMExchangeServerConnectorSecuritySetting
titleSuffix: Configuration Manager
description: Configures security options for a Microsoft Exchange Server connector in Configuration Manager.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833679
schema: 2.0.0
ms.assetid: 3B5B71A1-F88F-4699-8D6F-534921DA754D
>>>>>>> master
---

# New-CMExchangeServerConnectorSecuritySetting

## SYNOPSIS
Configures security options for a Microsoft Exchange Server connector in Configuration Manager.

## SYNTAX

```
New-CMExchangeServerConnectorSecuritySetting [-Bluetooth <BluetoothConnectionType>] [-Browser <Boolean>]
 [-Camera <Boolean>] [-FileEncrypt <Boolean>] [-Infrared <Boolean>] [-RemoteDesktop <Boolean>]
 [-StorageCard <Boolean>] [-StorageCardEncrypt <Boolean>] [-TextMessage <Boolean>] [-WifiConnection <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServerConnectorSecuritySetting** cmdlet configures security options for a Microsoft Exchange Server connector in Microsoft System Center Configuration Manager.
An Exchange Server connector in System Center Configuration Manager manages mobile devices that connect to an on-premise or online Exchange Server by using the Exchange ActiveSync protocol.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Configure security settings for a mobile device
```
PS XYZ:\> New-CMExchangeServerConnectorSecuritySetting -RemoteDesktop $True -StorageCard $True -Camera $True -Bluetooth $False -WiFiConnection HandsfreeOnly -Infra $False -Browser $False -StorageCardEncrypt $False -FileEncrypt $False -TextMessage $False
```

This command sets the following security options for a mobile device:

- Enables the camera. 
- Disables Bluetooth, infrared communications, file encryption on storage cards, and text messaging.
- Allows the mobile device to connect to the Internet only when the device is in hands-free mode.

## PARAMETERS

### -Bluetooth
Indicates whether users can run Bluetooth on the mobile device.

```yaml
Type: BluetoothConnectionType
Parameter Sets: (All)
Aliases: 
Accepted values: Disable, HandsfreeOnly, Allow
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Browser
Indicates whether users can use the browser on the mobile device.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Camera
Indicates whether users can use the camera on the mobile device.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
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

### -FileEncrypt
Indicates whether users can encrypt files on the mobile device.

```yaml
Type: Boolean
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

### -Infrared


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Infra
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteDesktop
Indicates whether a device can initiate a Remote Desktop connection.
This policy setting requires an Exchange Enterprise Client Access License.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageCard
Indicates whether the mobile device can access information on a storage card.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageCardEncrypt
Indicates whether the mobile device encrypts new files on the storage card by using a key that is tied to the device.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TextMessage
Indicates whether the user can send and receive SMS and MMS text messages with the mobile device.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WifiConnection
Specifies whether the user can use Wireless (Wi-Fi) local area networks (LANs) with the device.
Valid values are: 

- Allow
- Disable
- HandsfreeOnly

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorAccessRule](New-CMExchangeServerConnectorAccessRule.md)

[New-CMExchangeServerConnectorApplicationSetting](New-CMExchangeServerConnectorApplicationSetting.md)

[New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorPasswordSetting](New-CMExchangeServerConnectorPasswordSetting.md)
