---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMExchangeConnectorApplicationSetting

## SYNOPSIS
Creates application-related settings for a mobile device that uses a Exchange Server connector.

## SYNTAX

```
New-CMExchangeConnectorApplicationSetting [-UnsignedInstall <Boolean>] [-UnsignedApplication <Boolean>]
 [-BlockedApplication <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeConnectorApplicationSetting** cmdlet creates application-related settings for a mobile device that uses a Microsoft Exchange Server connector.

## EXAMPLES

### Example 1: Set application options for an Exchange Server connector
```
PS C:\> New-CMExchangeServerConnectorApplicationSetting -UnsignedApplication $False -UnsignedInstall $True -BlockedApplication "a1","a2"
```

This command sets these application options for an Exchange Server connector: 

- Allows the mobile device to install unsigned applications.
- Blocks unsigned applications from running on the mobile device.
- Blocks the two applications named a1 and a2 from running.

## PARAMETERS

### -BlockedApplication
{{Fill BlockedApplication Description}}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
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

### -UnsignedApplication
{{Fill UnsignedApplication Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UnsignedInstall
{{Fill UnsignedInstall Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.HS.Commands.ExchangeConnectorApplicationSetting

## NOTES

## RELATED LINKS

[New-CMExchangeConnectorAccessRule](./New-CMExchangeConnectorAccessRule.md)

[New-CMExchangeConnectorEmailManagementSetting](./New-CMExchangeConnectorEmailManagementSetting.md)

[New-CMExchangeConnectorPasswordSetting](./New-CMExchangeConnectorPasswordSetting.md)

[New-CMExchangeConnectorSecuritySetting](./New-CMExchangeConnectorSecuritySetting.md)
