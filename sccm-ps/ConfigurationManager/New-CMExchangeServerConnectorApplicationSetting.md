---
author: aczechowski
description: Creates application-related settings for a mobile device that uses a Exchange Server connector.
external help file:
manager: dougeby
Module Name: AdminUI.PS.HS
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMExchangeServerConnectorApplicationSetting
titleSuffix: Configuration Manager
---

# New-CMExchangeServerConnectorApplicationSetting

## SYNOPSIS
Creates application-related settings for a mobile device that uses a Exchange Server connector.

## SYNTAX

## DESCRIPTION
The **New-CMExchangeServerConnectorApplicationSetting** cmdlet creates application-related settings for a mobile device that uses a Microsoft Exchange Server connector.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Set application options for an Exchange Server connector
```
PS XYZ:\> New-CMExchangeServerConnectorApplicationSetting -UnsignedApplication $False -UnsignedInstall $True -BlockedApplication "a1","a2"
```

This command sets these application options for an Exchange Server connector:

- Allows the mobile device to install unsigned applications.
- Blocks unsigned applications from running on the mobile device.
- Blocks the two applications named a1 and a2 from running.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorAccessRule](New-CMExchangeServerConnectorAccessRule.md)

[New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorPasswordSetting](New-CMExchangeServerConnectorPasswordSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md)


