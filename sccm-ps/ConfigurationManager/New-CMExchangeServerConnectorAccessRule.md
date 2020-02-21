---
author: aczechowski
description: Configures access settings for a mobile device that uses a Microsoft Exchange Server connector.
external help file:
manager: dougeby
Module Name: AdminUI.PS.HS
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMExchangeServerConnectorAccessRule
titleSuffix: Configuration Manager
---

# New-CMExchangeServerConnectorAccessRule

## SYNOPSIS
Configures access settings for a mobile device that uses a Microsoft Exchange Server connector.

## SYNTAX

## DESCRIPTION
The **New-CMExchangeServerConnectorAccessRule** cmdlet configures access settings for a mobile device that uses a Microsoft Exchange Server connector.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Configure email management settings for a mobile device
```
PS XYZ:\> New-CMExchangeServerConnectorAccessRule -RuleName "AccessRule01" -AccessLevel Allow -Device DeviceType
```

This command creates an access rule for a device type named AccessRule01 that has the Allow access level.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorApplicationSetting](New-CMExchangeServerConnectorApplicationSetting.md)

[New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorPasswordSetting](New-CMExchangeServerConnectorPasswordSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md)


