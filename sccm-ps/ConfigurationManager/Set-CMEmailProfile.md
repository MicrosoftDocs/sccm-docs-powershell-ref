---
description: Sets an email profile.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMEmailProfile
---

# Set-CMEmailProfile

## SYNOPSIS
Sets an email profile.

## SYNTAX

### ByValue (Default)
```
Set-CMEmailProfile [-AccountDomainActiveDirectory <String>] [-AccountDomainCustom <String>]
 [-AccountName <String>] [-AccountUserNameType <String>] [-AllowMessageMove <Boolean>]
 [-AllowThirdPartyApplication <Boolean>] [-Description <String>] [-EmailAddressType <String>]
 [-EnableSmime <Boolean>] [-IdentityCertificate <IResultObject>] -InputObject <IResultObject>
 [-MailSyncDays <MailNumberofDaysToSync>] [-NewName <String>] [-PassThru] [-SigningCertificate <IResultObject>]
 [-SupportedPlatform <IResultObject[]>] [-SyncContentType <EasProfileSyncContentType>]
 [-SynchronizeRecentlyUsed <Boolean>] [-SyncSchedule <Schedule>] [-UseSsl <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMEmailProfile [-AccountDomainActiveDirectory <String>] [-AccountDomainCustom <String>]
 [-AccountName <String>] [-AccountUserNameType <String>] [-AllowMessageMove <Boolean>]
 [-AllowThirdPartyApplication <Boolean>] [-Description <String>] [-EmailAddressType <String>]
 [-EnableSmime <Boolean>] -Id <Int32> [-IdentityCertificate <IResultObject>]
 [-MailSyncDays <MailNumberofDaysToSync>] [-NewName <String>] [-PassThru] [-SigningCertificate <IResultObject>]
 [-SupportedPlatform <IResultObject[]>] [-SyncContentType <EasProfileSyncContentType>]
 [-SynchronizeRecentlyUsed <Boolean>] [-SyncSchedule <Schedule>] [-UseSsl <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMEmailProfile [-AccountDomainActiveDirectory <String>] [-AccountDomainCustom <String>]
 [-AccountName <String>] [-AccountUserNameType <String>] [-AllowMessageMove <Boolean>]
 [-AllowThirdPartyApplication <Boolean>] [-Description <String>] [-EmailAddressType <String>]
 [-EnableSmime <Boolean>] [-IdentityCertificate <IResultObject>] [-MailSyncDays <MailNumberofDaysToSync>]
 -Name <String> [-NewName <String>] [-PassThru] [-SigningCertificate <IResultObject>]
 [-SupportedPlatform <IResultObject[]>] [-SyncContentType <EasProfileSyncContentType>]
 [-SynchronizeRecentlyUsed <Boolean>] [-SyncSchedule <Schedule>] [-UseSsl <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMEmailProfile** cmdlet updates the settings of an Exchange ActiveSync email profile.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Update a profile by name
```
PS XYZ:\> Set-CMEmailProfile -Name "EmailProfile1" -NewName "newEmailProfile1"
```

This command updates the name of the Exchange ActiveSync email profile from EmailProfile1 to newEmailProfile1.

### Example 2: Update a profile by ID
```
PS XYZ:\> Set-CMEmailProfile -Id 16795654 -NewName "newEmailProfile2"
```

This command updates the name of the Exchange ActiveSync email profile with the ID of 16795654 to newEmailProfile2.

### Example 3: Update a profile as an input object
```
PS XYZ:\> $EmailProfile = Get-CMEmailProfile -Name "EmailProfile3"
PS XYZ:\> Set-CMEmailProfile -InputObject $EmailProfile -NewName "newEmailProfile3"
```

The first command gets the Exchange ActiveSync email profile object named EmailProfile3 and stores the object in the $EmailProfile variable.

The second command changes the name of the email profile stored in $EmailProfile to newEmailProfile3.

### Example 4: Use the pipeline to update a profile
```
PS XYZ:\> Get-CMEmailProfile -Name "EmailProfile4" | Set-CMEmailProfile -NewName "newEmailProfile4"
```

This command gets the Exchange ActiveSync email profile object named EmailProfile4 and uses the pipeline operator to pass the object to **Set-CMEmailProfile**, which changes the name of the email profile object to newEmailProfile4.

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

Required: False
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
Indicate whether users are allowed to move email messages between different accounts they have configured on their device.

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

### -AllowThirdPartyApplication
Indicates whether users are allowed to send email from certain non-default, third-party email applications.

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
Indicates whether outgoing email is sent using S/MIME encryption.

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

### -Id
Specifies the CI_ID for an Exchange ActiveSync email profile.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CI_ID, CIId

Required: True
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

### -InputObject
Specifies an Exchange ActiveSync email profile object.
To obtain an email profile object, use the Get-CMEmailProfile function.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Specifies the name of an Exchange ActiveSync email profile.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for an Exchange ActiveSync email profile.

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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

Required: False
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

### -SynchronizeRecentlyUsed
Indicates whether the list of email addresses that have been recently used on the device is synchronized.

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

### -UseSsl
Indicates whether Secure Sockets Layer (SSL) communication is used when sending emails, receiving emails, and communicating with the Exchange Server.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMConfigurationPolicy](Get-CMConfigurationPolicy.md)

[Get-CMEmailProfile](Get-CMEmailProfile.md)

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[New-CMEmailProfile](New-CMEmailProfile.md)


