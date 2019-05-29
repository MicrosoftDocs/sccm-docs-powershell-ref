---
title: New-CMExchangeServerConnectorEmailManagementSetting
titleSuffix: Configuration Manager
description: Creates a set of email management settings for a mobile device that uses an Exchange Server connector.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# New-CMExchangeServerConnectorEmailManagementSetting

## SYNOPSIS
Creates a set of email management settings for a mobile device that uses an Exchange Server connector.

## SYNTAX

```
New-CMExchangeServerConnectorEmailManagementSetting [-AllowHtmlEmail <Boolean>] [-ConsumerEmail <Boolean>]
 [-EmailAttachmentPolicy <Boolean>] [-MaximumCalendarAge <MaxCalendarAgeType>]
 [-MaximumEmailAge <MaxEmailAgeType>] [-MaximumSizeAttachment <Int32>] [-MaximumSizeHtmlEmail <Int32>]
 [-MaximumSizeTextEmail <Int32>] [-PushWhenRoaming <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServerConnectorEmailManagementSetting** cmdlet creates a set of e-mail management settings for a mobile device that uses an Exchange Server connector.

## EXAMPLES

### Example 1: Add email management settings to a mobile device
```
PS C:\> New-CMExchangeServerConnectorEmailManagementSetting -AllowHtmlEmail $True -ConsumerEmail $True -EmailAttachmentPolicy $True -MaximumCalenderAge ThreeMonths -MaximumEmailAge OneDay -PushWhenRoaming $True -MaximumSizeAttachment 24 -MaximumSizeHtmlEmail 402 -MaximumSizeTextEmail 401
```

This command creates the following settings for a mobile device: 

- Saves email data for one day before erasing it.
 
- Saves calendar data for three months before erasing it.
 
- Allows HTML-formatted email. 
- Sets a maximum size of 401 KB for text-formatted email and of 402 KB for HTML-formatted email. 
- Sets a maximum attachment size of 24 KB.

## PARAMETERS

### -AllowHtmlEmail
Indicates whether the mobile devices use HTML for e-mail messages.

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

### -ConsumerEmail
Indicates whether to allow consumer email through the connector.

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

### -EmailAttachmentPolicy
Indicates whether the policy allows email attachments.

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

### -MaximumCalendarAge


```yaml
Type: MaxCalendarAgeType
Parameter Sets: (All)
Aliases: MaximumCalenderAge
Accepted values: All, TwoWeeks, OneMonth, ThreeMonths, SixMonths
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumEmailAge
Specifies how long a mobile device saves email before the device automatically deletes the mail.
The acceptable values for this parameter are:

- OneDay
- OneMonth
- OneWeek
- ThreeDays
- TwoWeeks

```yaml
Type: MaxEmailAgeType
Parameter Sets: (All)
Aliases: 
Accepted values: All, OneDay, ThreeDays, OneWeek, TwoWeeks, OneMonth
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumSizeAttachment
Specifies the maximum size, in kilobytes (KB), for email attachments.

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

### -MaximumSizeHtmlEmail
Specifies the maximum size, in kilobytes, for HTML-formatted email.

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

### -MaximumSizeTextEmail
Specifies the maximum size, in kilobytes, for text-formatted email.

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

### -PushWhenRoaming
Indicates whether to push email to roaming clients.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorAccessRule](New-CMExchangeServerConnectorAccessRule.md)

[New-CMExchangeServerConnectorApplicationSetting](New-CMExchangeServerConnectorApplicationSetting.md)

[New-CMExchangeServerConnectorPasswordSetting](New-CMExchangeServerConnectorPasswordSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md)


