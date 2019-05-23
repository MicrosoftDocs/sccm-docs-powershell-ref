---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMExchangeConnectorAccessRule

## SYNOPSIS
Configures access settings for a mobile device that uses a Microsoft Exchange Server connector.

## SYNTAX

```
New-CMExchangeConnectorAccessRule -RuleName <String> -AccessLevel <AccessLevelType> -Device <DeviceType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServerConnectorAccessRule** cmdlet configures access settings for a mobile device that uses a Microsoft Exchange Server connector.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Configure email management settings for a mobile device
```
PS XYZ:\> New-CMExchangeServerConnectorAccessRule -RuleName "AccessRule01" -AccessLevel Allow -Device DeviceType
```

This command creates an access rule for a device type named AccessRule01 that has the Allow access level.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.HS.Commands.ExchangeConnectorAccessRule

## NOTES

## RELATED LINKS

[New-CMExchangeConnectorApplicationSetting](New-CMExchangeConnectorApplicationSetting.md)

[New-CMExchangeConnectorEmailManagementSetting](New-CMExchangConnectorEmailManagementSetting.md)

[New-CMExchangeConnectorPasswordSetting](New-CMExchangeConnectorPasswordSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeConnectorSecuritySetting.md)
