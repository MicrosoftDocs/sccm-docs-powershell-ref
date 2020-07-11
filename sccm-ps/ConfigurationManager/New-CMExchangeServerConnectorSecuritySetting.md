---
description: Configures security options for a Microsoft Exchange Server connector in Configuration Manager.
external help file:
Module Name: AdminUI.PS.HS
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMExchangeServerConnectorSecuritySetting
---

# New-CMExchangeServerConnectorSecuritySetting

## SYNOPSIS
Configures security options for a Microsoft Exchange Server connector in Configuration Manager.

## SYNTAX

## DESCRIPTION
The **New-CMExchangeServerConnectorSecuritySetting** cmdlet configures security options for a Microsoft Exchange Server connector in Microsoft System Center Configuration Manager.
An Exchange Server connector in System Center Configuration Manager manages mobile devices that connect to an on-premise or online Exchange Server by using the Exchange ActiveSync protocol.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Configure security settings for a mobile device
```
PS XYZ:\> New-CMExchangeServerConnectorSecuritySetting -RemoteDesktop $True -StorageCard $True -Camera $True -Bluetooth $False -WiFiConnection HandsfreeOnly -Infra $False -Browser $False -StorageCardEncrypt $False -FileEncrypt $False -TextMessage $False
```

This command sets the following security options for a mobile device:

- Enables the camera.
- Disables Bluetooth, infrared communications, file encryption on storage cards, and text messaging.
- Allows the mobile device to connect to the Internet only when the device is in hands-free mode.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.HS.Commands.ExchangeConnectorSecuritySetting

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorAccessRule](New-CMExchangeServerConnectorAccessRule.md)

[New-CMExchangeServerConnectorApplicationSetting](New-CMExchangeServerConnectorApplicationSetting.md)

[New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorPasswordSetting](New-CMExchangeServerConnectorPasswordSetting.md)
