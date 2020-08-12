---
description: Configure access settings for a mobile device that uses a Microsoft Exchange Server connector.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/30/2020
schema: 2.0.0
title: New-CMExchangeConnectorAccessRule
---

# New-CMExchangeConnectorAccessRule

## SYNOPSIS

Configure access settings for a mobile device that uses a Microsoft Exchange Server connector.

## SYNTAX

```
New-CMExchangeConnectorAccessRule -RuleName <String> -AccessLevel <AccessLevelType> -Device <DeviceType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeConnectorAccessRule** cmdlet configures access settings for a mobile device that uses a Microsoft Exchange Server connector.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Configure email management settings for a mobile device

This command creates an access rule for a device type named **AccessRule01** that has the **Allow** access level.

```powershell
New-CMExchangeConnectorAccessRule -RuleName "AccessRule01" -AccessLevel Allow -Device DeviceType
```

## PARAMETERS

### -AccessLevel
```yaml
Type: AccessLevelType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Quarantine

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Device
```yaml
Type: DeviceType
Parameter Sets: (All)
Aliases:
Accepted values: DeviceType, DeviceModel

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

### -RuleName
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.HS.Commands.ExchangeConnectorAccessRule

## NOTES

Cmdlet aliases: **New-CMExchangeServerConnectorAccessRule**

## RELATED LINKS

[New-CMExchangeConnectorApplicationSetting](New-CMExchangeConnectorApplicationSetting.md)

[New-CMExchangeConnectorEmailManagementSetting](New-CMExchangeConnectorEmailManagementSetting.md)

[New-CMExchangeConnectorPasswordSetting](New-CMExchangeConnectorPasswordSetting.md)

[New-CMExchangeConnectorSecuritySetting](New-CMExchangeConnectorSecuritySetting.md)
