---
author: aczechowski
description: Gets a Configuration Manager Exchange Server object.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMExchangeServer
titleSuffix: Configuration Manager
---

# Get-CMExchangeServer

## SYNOPSIS
Gets a Configuration Manager Exchange Server object.

## SYNTAX

```
Get-CMExchangeServer [-SiteCode <String>] [-ExchangeServerUrl <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMExchangeServer** cmdlet gets an object that represents a Microsoft Exchange Server that Microsoft System Center Configuration Manager uses.

Configuration Manager works with Exchange Server to manage mobile devices that cannot run Configuration Manager clients.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get all Exchange Server systems
```
PS XYZ:\> Get-CMExchangeServer
```

This command gets all the Exchange Server items for a Configuration Manager server.

### Example 2: Get an Exchange Server for a site
```
PS XYZ:\> Get-CMExchangeServer -SiteCode "PE1"
```

This command gets an Exchange Server for the site identified by the site code PE1.

### Example 3: Get a specified nextref_exchange
```
PS XYZ:\> Get-CMExchangeServer -Address "http://localhost/PowerShell"
```

This command gets the Exchange Server with the specified address.

## PARAMETERS

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -ExchangeServerUrl
```yaml
Type: String
Parameter Sets: (All)
Aliases: Address

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -SiteCode
Specifies the site code for a Configuration Manager site associated with the Exchange Server.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServer](New-CMExchangeServer.md)

[Remove-CMExchangeServer](Remove-CMExchangeServer.md)

[Set-CMExchangeServer](Set-CMExchangeServer.md)

[Sync-CMExchangeServer](Sync-CMExchangeServer.md)


