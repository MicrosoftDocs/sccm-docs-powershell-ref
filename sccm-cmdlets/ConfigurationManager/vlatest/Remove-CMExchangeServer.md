---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834104
schema: 2.0.0
ms.assetid: 5BF0061A-3EB7-4D64-BA08-72AD7E25B4DC
---

# Remove-CMExchangeServer

## SYNOPSIS
Removes an Exchange Server object from Configuration Manager.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Remove-CMExchangeServer [-SiteCode <String>] -ExchangeServerUrl <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValue
```
Remove-CMExchangeServer [-Force] -InputObject <ExchangeConnector> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMExchangeServer** cmdlet removes a Microsoft Exchange Server object from Microsoft System Center Configuration Manager for one or more Configuration Manager sites.
This cmdlet does not uninstall the Exchange Server.

Configuration Manager works with Exchange Server to manage mobile devices that cannot run Configuration Manager clients.

## EXAMPLES

### Example 1: Remove an nextref_exchange
```
PS C:\>Remove-CMExchangeServer -Address "http://localhost/PowerShell" -SiteCode "PE1"
```

This command removes the Exchange Server with the specified address for the site code PE1.

## PARAMETERS

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

### -ExchangeServerUrl


```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases: Address, ServerAddress
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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

### -InputObject


```yaml
Type: ExchangeConnector
Parameter Sets: ByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site associated with the Exchange Server.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
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

[Get-CMExchangeServer](./Get-CMExchangeServer.md)

[New-CMExchangeServer](./New-CMExchangeServer.md)

[Set-CMExchangeServer](./Set-CMExchangeServer.md)

[Sync-CMExchangeServer](./Sync-CMExchangeServer.md)


