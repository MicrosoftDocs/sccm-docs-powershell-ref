---
description: Create application-related settings for a mobile device that uses a Exchange Server connector.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/30/2020
schema: 2.0.0
title: New-CMExchangeConnectorApplicationSetting
---

# New-CMExchangeConnectorApplicationSetting

## SYNOPSIS

Create application-related settings for a mobile device that uses a Exchange Server connector.

## SYNTAX

```
New-CMExchangeConnectorApplicationSetting [-BlockedApplication <String[]>] [-UnsignedApplication <Boolean>]
 [-UnsignedInstall <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMExchangeConnectorApplicationSetting** cmdlet creates application-related settings for a mobile device that uses a Microsoft Exchange Server connector.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set application options for an Exchange Server connector

This command sets these application options for an Exchange Server connector:

- Allows the mobile device to install unsigned applications.
- Blocks unsigned applications from running on the mobile device.
- Blocks the two applications named a1 and a2 from running.

```powershell
New-CMExchangeConnectorApplicationSetting -UnsignedApplication $False -UnsignedInstall $True -BlockedApplication "a1","a2"
```

## PARAMETERS

### -BlockedApplication
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

### -UnsignedApplication
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.HS.Commands.ExchangeConnectorApplicationSetting

## NOTES

Cmdlet aliases: **New-CMExchangeServerConnectorApplicationSetting**

## RELATED LINKS

[New-CMExchangeConnectorAccessRule](New-CMExchangeConnectorAccessRule.md)

[New-CMExchangeConnectorEmailManagementSetting](New-CMExchangeConnectorEmailManagementSetting.md)

[New-CMExchangeConnectorPasswordSetting](New-CMExchangeConnectorPasswordSetting.md)

[New-CMExchangeConnectorSecuritySetting](New-CMExchangeConnectorSecuritySetting.md)
