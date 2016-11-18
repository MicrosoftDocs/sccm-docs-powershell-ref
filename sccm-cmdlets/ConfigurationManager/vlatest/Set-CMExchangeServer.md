---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 660FDB95-D970-4937-8A63-1EC4219625CA
---

# Set-CMExchangeServer

## SYNOPSIS
Changes settings for an Exchange server.

## SYNTAX

```
Set-CMExchangeServer [-SiteCode <String>] -ServerAddress <String> [-NewServerAddress <String>]
 [-IsHosted <Boolean>] [-ExchangeClientAccessServer <Dictionary`2[]>] [-UserName <String>]
 [-FullSyncSchedule <IResultObject>] [-DeltaSyncMins <Int32>] [-MaximumInactiveDays <Int32>] [-FindAll]
 [-ActiveDirectoryContainer <String[]>] [-GeneralSetting <ExchangeConnectorGeneralSetting>]
 [-PasswordSetting <ExchangeConnectorPasswordSetting>]
 [-EmailManagementSetting <ExchangeConnectorEmailManagementSetting>]
 [-SecuritySetting <ExchangeConnectorSecuritySetting>]
 [-ApplicationSetting <ExchangeConnectorApplicationSetting>] [-AllowExternalDeviceManagement <Boolean>]
 [-EnableAccessRule <Boolean>] [-AccessLevel <AccessLevelType>] [-AccessRule <ExchangeConnectorAccessRule[]>]
 [-EmailAddress <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMExchangeServer** cmdlet changes settings for a Microsoft Exchange Server.

Microsoft System Center Configuration Manager works with Exchange Server to manage mobile devices that cannot run Configuration Manager clients.

## EXAMPLES

### Example 1: Change settings for an nextref_exchange
```
PS C:\>$Gs= New-CMExchangeServerConnectorGeneralSetting -AllowInternetShare $True -AllowDesktopSync $True -AllowNonProvision $True -RefreshInterval 4
PS C:\> $Ps= New-CMExchangeServerConnectorPasswordSetting -PasswordEnabled $True -MinimumPasswordLength 8 -PasswordExpiration 51 -PasswordHistory 21 -WipeAfterFailedAttempt 6 -MaximumIdleTimeMinutes 41 -PasswordComplexity
PS C:\> $Em = New-CMExchangeServerConnectorEmailManagementSetting -ConsumerEmail $True -MaximumEmailAge OneDay -MaximumCalenderAge ThreeMonths -PushWhenRoaming $True -AllowHtmlEmail $True -EmailAttachmentPolicy $True -MaximumSizeTextEmail 401 -MaximumSizeHtmlEmail 402 -MaximumSizeAttachment 24
PS C:\> $Ss = New-CMExchangeServerConnectorSecuritySetting -RemoteDesktop $True -StorageCard $True -Camera $True -Bluetooth $False -WiFiConnection HandsfreeOnly -Infra $False -Browser $False -StorageCardEncrypt $False -FileEncrypt $False -TextMessage $False
PS C:\> $As= New-CMExchangeServerConnectorApplicationSetting -UnsignedInstall $True -UnsignedApplication $False -BlockedApplication "App01","App02"
PS C:\> Set-CMExchangeServer -SiteCode "CM2" -ServerAddress "http://www.contoso.com/powershell" -NewServerAddress "www.fabrikam.com" -UserName "ElisaDaugherty@contoso.com" -DeltaSyncInterval 124 -MaximumInactiveDay 26 -FindAll -AllowExternalDeviceManagement $False -EnableAccessRule $True -AccessLevel Allow -EmailAddress "EvanNarvaez@fabrikam.com","DavidChew@contosco.com" -GeneralSetting $Gs -PasswordSetting $Ps -EmailManagementSetting $Em -SecuritySetting $Ss -ApplicationSetting $As
```

The first command uses the New-CMExchangeServerConnectorGeneralSetting cmdlet to add new settings to an Exchange Server connector in Configuration Manager, and stores the settings in the $Gs variable.

The second command uses the New-CMExchangeServerConnectorPasswordSetting cmdlet adds new password settings to an Exchange Server connector in Configuration Manager, and stores the password settings in the $Ps variable.

The third command uses the New-CMExchangeServerConnectorEmailManagementSetting cmdlet creates a set of e-mail management settings for a mobile device that uses an Exchange Server connector, and stores the password settings in the $Em variable.

The fourth command uses the New-CMExchangeServerConnectorSecuritySetting cmdlet configures security options for an Exchange Server connector in Configuration Manager, and security settings in the $Ss variable.

The fifth command uses the New-CMExchangeServerConnectorApplicationSetting cmdlet creates application-related settings for a mobile device that uses an Exchange Server connector, and stores the application settings in the $As variable.

The final command changes settings for an Exchange Server for the Configuration Manager site that has the site code CM2.
The command specifies the general settings for the Exchange Server connector stored in $Gs.
The command specifies password settings for the Exchange Server connector stored in $Ps.
The command specifies a set of e-mail management settings for the Exchange Server connector stored in $Em.
The command specifies the security options for the Exchange Server connector stored in $Ss.
The command specifies application-related settings for a mobile device stored in $As.

## PARAMETERS

### -AccessLevel


```yaml
Type: AccessLevelType
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Block, Quarantine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccessRule


```yaml
Type: ExchangeConnectorAccessRule[]
Parameter Sets: (All)
Aliases: AccessRules

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryContainer


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ActiveDirectoryContainers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowExternalDeviceManagement


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

Required: False
Position: Named
Default value: None
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

### -EmailAddress


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: EmailAddresses

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailManagementSetting


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

### -EnableAccessRule


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

### -ExchangeClientAccessServer


```yaml
Type: Dictionary`2[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FindAll


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

### -FullSyncSchedule


```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeneralSetting


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

### -IsHosted


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

### -MaximumInactiveDays


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumInactiveDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewServerAddress


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

### -PasswordSetting


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

[New-CMExchangeServerConnectorApplicationSetting](./New-CMExchangeServerConnectorApplicationSetting.md)

[New-CMExchangeServerConnectorEmailManagementSetting](./New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](./New-CMExchangeServerConnectorSecuritySetting.md)

[Remove-CMExchangeServer](./Remove-CMExchangeServer.md)

[Sync-CMExchangeServer](./Sync-CMExchangeServer.md)


