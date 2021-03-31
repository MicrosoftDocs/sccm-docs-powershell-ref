---
description: Creates a Client Access server role for an Exchange Server.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMExchangeClientAccessServer
---

# New-CMExchangeClientAccessServer

## SYNOPSIS
Creates a Client Access server role for an Exchange Server.

## SYNTAX

```
New-CMExchangeClientAccessServer -ActiveDirectorySiteName <String> -ExchangeClientAccessServerName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeClientAccessServer** cmdlet creates a Client Access server role for a Microsoft Exchange Server.
The Client Access server role accepts connections to Exchange Server from different types of clients.
Software clients such as Microsoft Outlook use POP3 or IMAP4 connections to communicate with Exchange Server.
Hardware clients, such as mobile devices, use ActiveSync, POP3, or IMAP4 to communicate with Exchange Server.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create an Exchange Client Access server
```
PS XYZ:\> $Ecs= New-CMExchangeClientAccessServer -ExchangeClientAccessServerName "ContosoWestCAS11" -ActiveDirectorySiteName "ContosoWestAD01"
```

This command creates a new Exchange Client Access server named ContosoWestCAS11 and associates it with the Active Directory site named ContosoWestAD01, then places the resulting Exchange Client Access server object in the variable $Ecs.

## PARAMETERS

### -ActiveDirectorySiteName
Specifies the name of the Active Directory site on which you are installing the Client Access server role.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

### -ExchangeClientAccessServerName
Specifies the name of the Exchange Client Access server that you create.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Collections.Generic.Dictionary`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## NOTES

## RELATED LINKS
