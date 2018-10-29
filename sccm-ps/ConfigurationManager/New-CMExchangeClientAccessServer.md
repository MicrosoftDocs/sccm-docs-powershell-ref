---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: E66BF7A0-762F-470D-BCD0-E0A58EA3FB6F
online version: https://go.microsoft.com/fwlink/?linkid=833654
schema: 2.0.0
---

# New-CMExchangeClientAccessServer

## SYNOPSIS
Creates a Client Access server role for an Exchange Server.

## SYNTAX

```
New-CMExchangeClientAccessServer -ExchangeClientAccessServerName <String> -ActiveDirectorySiteName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeClientAccessServer** cmdlet creates a Client Access server role for a Microsoft Exchange Server.
The Client Access server role accepts connections to Exchange Server from different types of clients.
Software clients such as Microsoft Outlook use POP3 or IMAP4 connections to communicate with Exchange Server.
Hardware clients, such as mobile devices, use ActiveSync, POP3, or IMAP4 to communicate with Exchange Server.

## EXAMPLES

### Example 1: Create an Exchange Client Access server
```
PS C:\> $Ecs= New-CMExchangeClientAccessServer -ExchangeClientAccessServerName "ContosoWestCAS11" -ActiveDirectorySiteName "ContosoWestAD01"
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

