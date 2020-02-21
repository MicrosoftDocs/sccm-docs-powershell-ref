---
author: aczechowski
description: Changes settings for an Exchange server.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMExchangeServer
titleSuffix: Configuration Manager
---

# Set-CMExchangeServer

## SYNOPSIS
Changes settings for an Exchange server.

## SYNTAX

```
Set-CMExchangeServer [-SiteCode <String>] -ServerAddress <String> [-NewServerAddress <String>]
 [-IsHosted <Boolean>] [-ExchangeClientAccessServer <Dictionary`2[]>] [-UserName <String>]
 [-NotificationUserName <String>] [-FullSyncSchedule <IResultObject>] [-DeltaSyncMins <Int32>]
 [-MaximumInactiveDays <Int32>] [-FindAll] [-ActiveDirectoryContainer <String[]>]
 [-GeneralSetting <ExchangeConnectorGeneralSetting>] [-PasswordSetting <ExchangeConnectorPasswordSetting>]
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

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Change settings for an nextref_exchange
```
PS XYZ:\> $Gs= New-CMExchangeServerConnectorGeneralSetting -AllowInternetShare $True -AllowDesktopSync $True -AllowNonProvision $True -RefreshInterval 4
PS XYZ:\> $Ps= New-CMExchangeServerConnectorPasswordSetting -PasswordEnabled $True -MinimumPasswordLength 8 -PasswordExpiration 51 -PasswordHistory 21 -WipeAfterFailedAttempt 6 -MaximumIdleTimeMinutes 41 -PasswordComplexity
PS XYZ:\> $Em = New-CMExchangeServerConnectorEmailManagementSetting -ConsumerEmail $True -MaximumEmailAge OneDay -MaximumCalenderAge ThreeMonths -PushWhenRoaming $True -AllowHtmlEmail $True -EmailAttachmentPolicy $True -MaximumSizeTextEmail 401 -MaximumSizeHtmlEmail 402 -MaximumSizeAttachment 24
PS XYZ:\> $Ss = New-CMExchangeServerConnectorSecuritySetting -RemoteDesktop $True -StorageCard $True -Camera $True -Bluetooth $False -WiFiConnection HandsfreeOnly -Infra $False -Browser $False -StorageCardEncrypt $False -FileEncrypt $False -TextMessage $False
PS XYZ:\> $As= New-CMExchangeServerConnectorApplicationSetting -UnsignedInstall $True -UnsignedApplication $False -BlockedApplication "App01","App02"
PS XYZ:\> Set-CMExchangeServer -SiteCode "CM2" -ServerAddress "http://www.contoso.com/powershell" -NewServerAddress "www.fabrikam.com" -UserName "ElisaDaugherty@contoso.com" -DeltaSyncInterval 124 -MaximumInactiveDay 26 -FindAll -AllowExternalDeviceManagement $False -EnableAccessRule $True -AccessLevel Allow -EmailAddress "EvanNarvaez@fabrikam.com","DavidChew@contosco.com" -GeneralSetting $Gs -PasswordSetting $Ps -EmailManagementSetting $Em -SecuritySetting $Ss -ApplicationSetting $As
```

The first command uses the **New-CMExchangeServerConnectorGeneralSetting** cmdlet to add new settings to an Exchange Server connector in Configuration Manager, and stores the settings in the $Gs variable.<!--505995-->

The second command uses the [New-CMExchangeServerConnectorPasswordSetting](New-CMExchangeServerConnectorPasswordSetting.md) cmdlet adds new password settings to an Exchange Server connector in Configuration Manager, and stores the password settings in the $Ps variable.

The third command uses the [New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md) cmdlet creates a set of e-mail management settings for a mobile device that uses an Exchange Server connector, and stores the password settings in the $Em variable.

The fourth command uses the [New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md) cmdlet configures security options for an Exchange Server connector in Configuration Manager, and security settings in the $Ss variable.

The fifth command uses the [New-CMExchangeServerConnectorApplicationSetting](New-CMExchangeServerConnectorApplicationSetting.md) cmdlet creates application-related settings for a mobile device that uses an Exchange Server connector, and stores the application settings in the $As variable.

The final command changes settings for an Exchange Server for the Configuration Manager site that has the site code CM2.
The command specifies the general settings for the Exchange Server connector stored in $Gs.
The command specifies password settings for the Exchange Server connector stored in $Ps.
The command specifies a set of e-mail management settings for the Exchange Server connector stored in $Em.
The command specifies the security options for the Exchange Server connector stored in $Ss.
The command specifies application-related settings for a mobile device stored in $As.

## PARAMETERS

### -AccessLevel
Specifies the type of access for the mobile devices.
Access level applies to a mobile device that is not managed by a rule.
Valid values are:

- Allow
- Block
- Quarantine

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
Specifies an array of names of Active Directory containers.
When this parameter appears, the Exchange Server connector searches for the device only in the Active Directory containers.

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
Specifies application settings, such as allow or deny the installation of applications.
For each dictionary entry in the array, specify the setting name as the key the configuration as the value.
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

### -EmailAddress
Specifies an array of email addresses.

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
Specifies email management settings, such as synchronization schedule, message format, and size of attachments.
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

### -EnableAccessRule
Indicates whether to enable an access rule.

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
Specifies Exchange Client Access servers, as key-value pairs.

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
Indicates that the discovery process find all mobile devices in an Exchange organization.

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

### -FullSyncSchedule
Specifies a result object that schedules the full discovery time for an Exchange Server connector.

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
Specifies general settings for mobile devices that use the Exchange Server Connector.
Settings you can specify for this parameter include:

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
Specifies a new server address for an Exchange server.

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

### -NotificationUserName
{{ Fill NotificationUserName Description }}

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
Specifies general password settings.
Settings you can specify for this parameter include:

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
Settings you can specify for this parameter include:

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
Specifies the Exchange Server by using a site code.

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
Specifies the user name that the connector uses to connect to the Exchange Server.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMExchangeServer](Get-CMExchangeServer.md)

[New-CMExchangeServer](New-CMExchangeServer.md)

[New-CMExchangeServerConnectorApplicationSetting](New-CMExchangeServerConnectorApplicationSetting.md)

[New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md)

[Remove-CMExchangeServer](Remove-CMExchangeServer.md)

[Sync-CMExchangeServer](Sync-CMExchangeServer.md)
