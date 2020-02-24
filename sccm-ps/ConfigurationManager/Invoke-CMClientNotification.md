---
author: aczechowski
description: Sends a notification to client computers to trigger an immediate client action.
external help file:
manager: dougeby
Module Name: AdminUI.PS.Collections
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Invoke-CMClientNotification
titleSuffix: Configuration Manager
---

# Invoke-CMClientNotification

## SYNOPSIS
Sends a notification to client computers to trigger an immediate client action.

## SYNTAX

## DESCRIPTION
The **Invoke-CMClientNotification** cmdlet sends a notification to client computers to trigger an immediate client action.
You can specify one or more client computers, or send a notification to all the computers in a specified device collection.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Send a notification to trigger an event
```
PS XYZ:\>Invoke-CMClientNotification -DeviceName "Computer073" -NotificationType RequestMachinePolicyNow
```

This command sends a notification of the type RequestMachinePolicyNow to the device named Computer073.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDevice](Get-CMDevice.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)


