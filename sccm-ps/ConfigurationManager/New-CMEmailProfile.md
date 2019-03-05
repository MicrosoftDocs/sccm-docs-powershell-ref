---
external help file: AdminUI.PS.Dcm.dll-Help.xml
ms.assetid: 8C11B11B-494E-4AE3-870D-ADBA8D5798BB
online version: https://go.microsoft.com/fwlink/?linkid=833637
schema: 2.0.0
---

# New-CMEmailProfile

## SYNOPSIS
Creates an email profile.

## SYNTAX

```
New-CMEmailProfile [-AccountDomainActiveDirectory <String>] [-AccountDomainCustom <String>]
 -AccountName <String> [-AccountUserNameType <String>] [-AllowMessageMove] [-AllowThirdPartyApplication]
 [-Description <String>] [-DoNotUseSsl] [-EmailAddressType <String>] [-EnableSmime] -ExchangeHost <String>
 [-IdentityCertificate <IResultObject>] [-MailSyncDays <MailNumberofDaysToSync>] -Name <String>
 [-SigningCertificate <IResultObject>] -SupportedPlatform <IResultObject[]>
 [-SyncContentType <EasProfileSyncContentType>] [-SynchronizeRecentlyUsed] [-SyncSchedule <Schedule>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMEmailProfile** cmdlet creates an Exchange ActiveSync email profile.

## EXAMPLES

### Example 1: Create an email profile
```
PS C:\> $Platform = Get-CMSupportedPlatform -Fast -Platform "Windows Phone"
PS C:\> New-CMEmailProfile -AccountName "TestAccount1" -ExchangeHost "TestHost1" -Name "EmailProfile01" -SupportedPlatform $Platform[1] -AccountUserNameType sAMAccountName -AccountDomainActiveDirectory domain
```

The first command gets all supported platform objects for Windows Phone and stores the objects in the $Platform variable.

The second command creates an email named EmailProfile01 using the second supported platform object from $Platform.

## PARAMETERS

### -AccountDomainActiveDirectory
Specifies the type of Active Directory account domain.
Valid values are: 

- domain
- ntdomain

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: domain, ntdomain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountDomainCustom
Specifies a custom account domain.
This parameter can only be used if the sAMAccountName value is specified for the *AccountUserNameType* parameter.

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

### -AccountName
Specifies the display name for the email account.

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

### -AccountUserNameType
Specifies an account user name type.
Valid values are: 

- mail
- sAMAccountName
- userPrincipalName

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: mail, sAMAccountName, userPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowMessageMove
Indicates that users are allowed to move email messages between different accounts they have configured on their device.

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

### -AllowThirdPartyApplication
Indicates that users are allowed to send email from certain non-default, third-party email applications.

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

### -Description
Specifies a description for the Exchange ActiveSync email profile.

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

### -DoNotUseSsl
Indicates that Secure Sockets Layer (SSL) communication is not used when sending emails, receiving emails, and communicating with the Exchange Server.

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

### -EmailAddressType
Specifies an email address type.
Valid values are: 

- mail
- userPrincipalName

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: mail, userPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSmime
Indicates that outgoing email is sent using S/MIME encryption.

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

### -ExchangeHost
Specifies the hostname of the Exchange server that hosts Exchange ActiveSync services.

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

### -IdentityCertificate
Specifies an identity certificate object.
To obtain an identity certificate object, use the Get-CMConfigurationPolicy cmdlet.

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

### -MailSyncDays
Specifies the number of days of email to synchronize.
Valid values are: 

- Unlimited
- OneDay
- ThreeDays
- OneWeek
- TwoWeeks
- OneMonth

```yaml
Type: MailNumberofDaysToSync
Parameter Sets: (All)
Aliases: 
Accepted values: Unlimited, OneDay, ThreeDays, OneWeek, TwoWeeks, OneMonth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the Exchange ActiveSync email profile.

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

### -SigningCertificate
Specifies a signing certificate object used for S/MIME signing.
To obtain a signing certificate object, use the Get-CMConfigurationPolicy cmdlet.

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

### -SupportedPlatform
Specifies the operating systems on which the email profile will be installed.
To obtain a supported platform object, use the Get-CMSupportedPlatform cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SupportedPlatforms

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncContentType
Specifies a content type to synchronize to devices.
Valid values are: 

- None
- Email
- Contacts 
- Calendar 
- Tasks 
- Notes
- All

```yaml
Type: EasProfileSyncContentType
Parameter Sets: (All)
Aliases: SyncContentTypes
Accepted values: None, Email, Contacts, Calendar, Tasks, Notes, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncSchedule
Specifies the schedule by which devices will synchronize data from the Exchange Server. 

- Manual
- FifteenMins
- ThirtyMins
- SixtyMins
- AsArrive

```yaml
Type: Schedule
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, FifteenMins, ThirtyMins, SixtyMins, AsArrive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SynchronizeRecentlyUsed
Indicates that the list of email addresses that have been recently used on the device is synchronized.

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

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Get-CMConfigurationPolicy](Get-CMConfigurationPolicy.md)

[Get-CMEmailProfile](Get-CMEmailProfile.md)

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[Set-CMEmailProfile](Set-CMEmailProfile.md)


