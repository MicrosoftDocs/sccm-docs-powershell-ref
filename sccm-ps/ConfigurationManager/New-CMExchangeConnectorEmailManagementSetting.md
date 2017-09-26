---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
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
{{Fill AllowHtmlEmail Description}}

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
{{Fill ConsumerEmail Description}}

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
{{Fill EmailAttachmentPolicy Description}}

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
{{Fill MaximumCalendarAge Description}}

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
{{Fill MaximumEmailAge Description}}

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
{{Fill MaximumSizeAttachment Description}}

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
{{Fill MaximumSizeHtmlEmail Description}}

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
{{Fill MaximumSizeTextEmail Description}}

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
{{Fill PushWhenRoaming Description}}

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

### Microsoft.ConfigurationManagement.Cmdlets.HS.Commands.ExchangeConnectorEmailManagementSetting

## NOTES

## RELATED LINKS

[New-CMExchangeConnectorAccessRule](New-CMExchangeConnectorAccessRule.md)

[New-CMExchangeConnectorApplicationSetting](New-CMExchangeConnectorApplicationSetting.md)

[New-CMExchangeConnectorPasswordSetting](New-CMExchangeConnectorPasswordSetting.md)

[New-CMExchangeConnectorSecuritySetting](New-CMExchangeConnectorSecuritySetting.md)
