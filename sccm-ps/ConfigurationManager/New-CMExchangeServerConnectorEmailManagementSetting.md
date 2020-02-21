---
author: aczechowski
description: Creates a set of email management settings for a mobile device that uses an Exchange Server connector.
external help file:
manager: dougeby
Module Name: AdminUI.PS.HS
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMExchangeServerConnectorEmailManagementSetting
titleSuffix: Configuration Manager
---

# New-CMExchangeServerConnectorEmailManagementSetting

## SYNOPSIS
Creates a set of email management settings for a mobile device that uses an Exchange Server connector.

## SYNTAX

## DESCRIPTION
The **New-CMExchangeServerConnectorEmailManagementSetting** cmdlet creates a set of e-mail management settings for a mobile device that uses an Exchange Server connector.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add email management settings to a mobile device
```
PS XYZ:\> New-CMExchangeServerConnectorEmailManagementSetting -AllowHtmlEmail $True -ConsumerEmail $True -EmailAttachmentPolicy $True -MaximumCalenderAge ThreeMonths -MaximumEmailAge OneDay -PushWhenRoaming $True -MaximumSizeAttachment 24 -MaximumSizeHtmlEmail 402 -MaximumSizeTextEmail 401
```

This command creates the following settings for a mobile device:

- Saves email data for one day before erasing it.

- Saves calendar data for three months before erasing it.

- Allows HTML-formatted email.
- Sets a maximum size of 401 KB for text-formatted email and of 402 KB for HTML-formatted email.
- Sets a maximum attachment size of 24 KB.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorAccessRule](New-CMExchangeServerConnectorAccessRule.md)

[New-CMExchangeServerConnectorApplicationSetting](New-CMExchangeServerConnectorApplicationSetting.md)

[New-CMExchangeServerConnectorPasswordSetting](New-CMExchangeServerConnectorPasswordSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md)


