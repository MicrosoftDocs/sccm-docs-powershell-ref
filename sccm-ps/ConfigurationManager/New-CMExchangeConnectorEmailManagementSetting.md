---
author: aczechowski
description: Creates a set of email management settings for a mobile device that uses an Exchange Server connector.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMExchangeConnectorEmailManagementSetting
titleSuffix: Configuration Manager
---

# New-CMExchangeConnectorEmailManagementSetting

## SYNOPSIS
Creates a set of email management settings for a mobile device that uses an Exchange Server connector.

## SYNTAX

```
New-CMExchangeConnectorEmailManagementSetting [-AllowHtmlEmail <Boolean>] [-ConsumerEmail <Boolean>]
 [-EmailAttachmentPolicy <Boolean>] [-MaximumCalendarAge <MaxCalendarAgeType>]
 [-MaximumEmailAge <MaxEmailAgeType>] [-MaximumSizeAttachment <Int32>] [-MaximumSizeHtmlEmail <Int32>]
 [-MaximumSizeTextEmail <Int32>] [-PushWhenRoaming <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeConnectorEmailManagementSetting** cmdlet creates a set of e-mail management settings for a mobile device that uses an Exchange Server connector.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add email management settings to a mobile device
```
PS XYZ:\> New-CMExchangeServerConnectorEmailManagementSetting -AllowHtmlEmail $True -ConsumerEmail $True -EmailAttachmentPolicy $True -MaximumCalenderAge ThreeMonths -MaximumEmailAge OneDay -PushWhenRoaming $True -MaximumSizeAttachment 24 -MaximumSizeHtmlEmail 402 -MaximumSizeTextEmail 401
```

This command creates the following settings for a mobile device:

- Saves email data for one day before erasing it.

- Saves calendar data for three months before erasing it.

- Allows HTML-formatted email.
- Sets a maximum size of 401 KB for text-formatted email and of 402 KB for HTML-formatted email.
- Sets a maximum attachment size of 24 KB.

## PARAMETERS

### -AllowHtmlEmail
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

### -EmailAttachmentPolicy
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

### Microsoft.ConfigurationManagement.cmdlets.HS.Commands.ExchangeConnectorEmailManagementSetting

## NOTES

## RELATED LINKS

[New-CMExchangeConnectorAccessRule](New-CMExchangeConnectorAccessRule.md)

[New-CMExchangeConnectorApplicationSetting](New-CMExchangeConnectorApplicationSetting.md)

[New-CMExchangeConnectorPasswordSetting](New-CMExchangeConnectorPasswordSetting.md)

[New-CMExchangeConnectorSecuritySetting](New-CMExchangeConnectorSecuritySetting.md)
