---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 6A49F9E5-ECD8-438F-9A2D-D0D2615941B3
online version: https://go.microsoft.com/fwlink/?linkid=833658
schema: 2.0.0
---

# New-CMExchangeServer

## SYNOPSIS
Configures a new Exchange Server connector.

## SYNTAX

### NewOnPrem (Default)
```
New-CMExchangeServer [-SiteCode <String>] -ServerAddress <String> [-IsHosted <Boolean>] [-OnPrem]
 [-ExchangeClientAccessServer <Dictionary`2[]>] [-UserName <String>] -FullSyncSchedule <IResultObject>
 -DeltaSyncMins <Int32> [-MaximumInactiveDay <Int32>] [-ActiveDirectoryContainer <String[]>]
 [-GeneralSetting <ExchangeConnectorGeneralSetting>] [-PasswordSetting <ExchangeConnectorPasswordSetting>]
 [-EmailManagementSetting <ExchangeConnectorEmailManagementSetting>]
 [-SecuritySetting <ExchangeConnectorSecuritySetting>]
 [-ApplicationSetting <ExchangeConnectorApplicationSetting>] [-AllowExternalDeviceManagement <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewHosted
```
New-CMExchangeServer [-SiteCode <String>] -ServerAddress <String> [-IsHosted <Boolean>] [-Hosted]
 -UserName <String> -FullSyncSchedule <IResultObject> -DeltaSyncMins <Int32> [-MaximumInactiveDay <Int32>]
 [-ActiveDirectoryContainer <String[]>] [-GeneralSetting <ExchangeConnectorGeneralSetting>]
 [-PasswordSetting <ExchangeConnectorPasswordSetting>]
 [-EmailManagementSetting <ExchangeConnectorEmailManagementSetting>]
 [-SecuritySetting <ExchangeConnectorSecuritySetting>]
 [-ApplicationSetting <ExchangeConnectorApplicationSetting>] [-AllowExternalDeviceManagement <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServer** cmdlet configures a new Microsoft Exchange Server connector in Microsoft System Center Configuration Manager.
An Exchange Server connector synchronizes and manages the device enrolled by the Exchange Server.
For more information, see [Configuration Manager 2012 Exchange Connector Implementation in Microsoft IT](http://go.microsoft.com/fwlink/?LinkId=286314) on TechNet.

## EXAMPLES

### Example 1: Create an Exchange Server
```
PS C:\> $schedule = New-CMSchedule -Start "03/01/2016 11:59 PM" -RecurInterval Days -RecurCount 1
PS C:\> New-CMExchangeServer -ServerAddress "http://exchange.contoso.com" -DeltaSyncInterval 120 -FullSyncSchedule $schedule -IsHosted -SiteCode "ContosoSite"
```

These commands create an Exchange Server with the server address `http://exchange.contoso.com`.
To do this, the first command in the example uses the **New-CMSchedule** cmdlet to create a schedule for doing Exchange synchronizations.
This schedule object is stored in a variable $schedule.

The second command then uses **New-CMExchangeServer** to create the new server as part of the site ContosoSite.

## PARAMETERS

### -ActiveDirectoryContainer
Specifies an array of names of Active Directory containers.
When this parameter is specified, the Exchange Server connector searches the Active Directory containers for the device.

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

### -AllowExternalDeviceManagement
Indicates whether an external device management program can manage the device.

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

### -ApplicationSetting
Specifies application settings.
For each dictionary entry in the array, specify the setting name as the key and the configuration as the value.
Valid values are: AllowUnsignedApplications, AllowUnsignedInstallationPackages, or Block a specific application.

```yaml
Type: ExchangeConnectorApplicationSetting
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

### -DeltaSyncMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DeltaSyncInterval

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

### -EmailManagementSetting
Specifies email management settings.
For each dictionary entry in the array, specify the setting name as the key and the configuration as the value.

```yaml
Type: ExchangeConnectorEmailManagementSetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExchangeClientAccessServer
Specifies an array of Exchange Client Access servers, as key-value pairs.

```yaml
Type: Dictionary`2[]
Parameter Sets: NewOnPrem
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

### -FullSyncSchedule
Specifies a result object that schedules the full discovery time for an Exchange Server connector.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeneralSetting
Specifies general settings.
Valid values are:

- RequireManualSyncWhenRoaming
- RequireStorageCardEncryption
- UnapprovedInROMApplicationList
- DevicePolicyRefreshInterval
- MaxInactivityTimeDeviceLock

```yaml
Type: ExchangeConnectorGeneralSetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hosted
```yaml
Type: SwitchParameter
Parameter Sets: NewHosted
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsHosted
Indicates that the Exchange Server connector configuration is for a hosted or on-premise Exchange Server.

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

### -MaximumInactiveDay
Specifies the interval between times that the Exchange Server connector runs device discovery.
The cmdlet checks the last sync time of the devices that Exchange Server manages.
If the most recent sync time is older than the current time - MinimumInactiveDay, then the exchange connector does not discover the devices.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnPrem
```yaml
Type: SwitchParameter
Parameter Sets: NewOnPrem
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordSetting
Specifies password settings.
Valid values are:

- AlphanumericDevicePasswordRequired
- DevicePasswordEnabled
- DevicePasswordExpiration
- DevicePasswordHistory
- MaxDevicePasswordFailedAttempts
- PasswordRecoveryEnabled
- MinDevicePasswordComplexCharacters
- MinDevicePasswordLength
- AlphanumericDevicePasswordRequired
- AllowSimpleDevicePassword

```yaml
Type: ExchangeConnectorPasswordSetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecuritySetting
Specifies a dictionary of security settings.
Valid values are: 

- AllowBluetooth
- AllowBrowser
- AllowCamera
- AllowDesktopSync
- AllowInternetSharing
- AllowIrDA
- AllowNonProvisionableDevices
- AllowRemoteDesktop
- AllowStorageCard
- AllowTextMessaging
- AllowWiFi

```yaml
Type: ExchangeConnectorSecuritySetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerAddress
Specifies the address of the Exchange Server for which the cmdlet configures the Exchange Server connector.

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

### -SiteCode
Specifies the site code of the Configuration Manager site where a Exchange Server connector runs.

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

### -UserName
Specifies the username that the connector uses to connect to the Exchange Server.

```yaml
Type: String
Parameter Sets: NewOnPrem
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NewHosted
Aliases: 

Required: True
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

[Get-CMExchangeServer](Get-CMExchangeServer.md)

[Remove-CMExchangeServer](Remove-CMExchangeServer.md)

[Set-CMExchangeServer](Set-CMExchangeServer.md)

[Sync-CMExchangeServer](Sync-CMExchangeServer.md)
