---
author: aczechowski
description: Adds new password settings to a Exchange Server connector in Configuration Manager.
external help file:
manager: dougeby
Module Name: AdminUI.PS.HS
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMExchangeServerConnectorPasswordSetting
titleSuffix: Configuration Manager
---

# New-CMExchangeServerConnectorPasswordSetting

## SYNOPSIS
Adds new password settings to a Exchange Server connector in Configuration Manager.

## SYNTAX

## DESCRIPTION
The **New-CMExchangeServerConnectorPasswordSetting** cmdlet adds new password settings to a Microsoft Exchange Server connector in Microsoft System Center Configuration Manager.
An Exchange Server connector in Configuration Manager manages mobile devices that connect to an on-premise or online Exchange Server by using the Exchange ActiveSync protocol.

## EXAMPLES

### Example 1: Specify password settings for an Exchange Server connector
```
PS XYZ:\> New-CMExchangeServerConnectorPasswordSetting -PasswordEnabled $True -MinimumPasswordLength 8 -PasswordExpiration 51 -PasswordHistory 21 -WipeAfterFailedAttempt 6 -MaximumIdleTimeMinutes 41 -PasswordComplexity Strong -MinimumComplexChar 3 -AllowSimplePassword $True -PasswordRecovery $True
```

This command sets these password-related options for an Exchange Server connector: 

- Requires the user to set a password on the mobile device. 
- Requires the password to have at least eight characters or digits. 
- Causes the password to expire after 51 days.
 
- Requires 21 password changes before the user can reuse an earlier password. 
- Wipes data from the mobile device after six failed attempts to change the password. 
- Allows 41 minutes to elapse before the mobile device locks itself. 
- Requires an alphanumeric password. 
- Allows passwords to be simple.
- Allows users to recover missing passwords from the mobile device.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md)


