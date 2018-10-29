---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMExchangeConnectorSecuritySetting

## SYNOPSIS
Configures security options for a Microsoft Exchange Server connector in Configuration Manager.

## SYNTAX

```
New-CMExchangeConnectorSecuritySetting [-Bluetooth <BluetoothConnectionType>] [-Browser <Boolean>]
 [-Camera <Boolean>] [-FileEncrypt <Boolean>] [-Infrared <Boolean>] [-RemoteDesktop <Boolean>]
 [-StorageCard <Boolean>] [-StorageCardEncrypt <Boolean>] [-TextMessage <Boolean>] [-WifiConnection <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServerConnectorSecuritySetting** cmdlet configures security options for a Microsoft Exchange Server connector in Microsoft System Center Configuration Manager.
An Exchange Server connector in System Center Configuration Manager manages mobile devices that connect to an on-premise or online Exchange Server by using the Exchange ActiveSync protocol.

## EXAMPLES

### Example 1: Configure security settings for a mobile device
```
PS C:\> New-CMExchangeServerConnectorSecuritySetting -RemoteDesktop $True -StorageCard $True -Camera $True -Bluetooth $False -WiFiConnection HandsfreeOnly -Infra $False -Browser $False -StorageCardEncrypt $False -FileEncrypt $False -TextMessage $False
```

This command sets the following security options for a mobile device:

- Enables the camera. 
- Disables Bluetooth, infrared communications, file encryption on storage cards, and text messaging.
- Allows the mobile device to connect to the Internet only when the device is in hands-free mode.

## PARAMETERS

### -Bluetooth
 

```yaml
Type: BluetoothConnectionType
Parameter Sets: (All)
Aliases: 
Accepted values: Disable, HandsfreeOnly, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Browser
 

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

### -Camera
 

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

### -FileEncrypt
 

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

### -Infrared
 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Infra

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteDesktop
 

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

### -StorageCard
 

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

### -StorageCardEncrypt
 

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

### -TextMessage
 

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

### -WifiConnection
 

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

### Microsoft.ConfigurationManagement.Cmdlets.HS.Commands.ExchangeConnectorSecuritySetting

## NOTES

## RELATED LINKS

[New-CMExchangeConnectorAccessRule](New-CMExchangeConnectorAccessRule.md)

[New-CMExchangeConnectorApplicationSetting](New-CMExchangeConnectorApplicationSetting.md)

[New-CMExchangeConnectorEmailManagementSetting](New-CMExchangeConnectorEmailManagementSetting.md)

[New-CMExchangeConnectorPasswordSetting](New-CMExchangeConnectorPasswordSetting.md)
