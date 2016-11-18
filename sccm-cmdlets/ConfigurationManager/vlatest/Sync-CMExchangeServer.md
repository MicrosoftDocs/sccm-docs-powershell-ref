---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 3FE27BD4-6193-4593-BCED-ABD609C55AC8
---

# Sync-CMExchangeServer

## SYNOPSIS
Synchronizes Configuration Manager mobile device information with an Exchange Server.

## SYNTAX

```
Sync-CMExchangeServer [-SiteCode <String>] -Address <String> [-Force] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Sync-CMExchangeServer** cmdlet synchronizes mobile device information with a specified Microsoft Exchange Server for one or more Configuration Manager sites.

Configuration Manager works with Exchange Server to manage mobile devices that cannot run Configuration Manager clients.

## EXAMPLES

### Example 1: Synchronize with an nextref_exchange
```
PS C:\>Sync-CMExchangeServer -Address "http://localhost/PowerShell" -SiteCode "PE1"
```

This command synchronizes mobile devices for the site that has the site code PE1 with the specified Exchange Server.

## PARAMETERS

### -Address
Specifies a URL for the Exchange Server.

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

### -PassThru


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

[Remove-CMExchangeServer](./Remove-CMExchangeServer.md)

[Set-CMExchangeServer](./Set-CMExchangeServer.md)


