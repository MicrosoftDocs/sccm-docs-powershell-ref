---
external help file: AdminUI.PS.Alerts.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834232
schema: 2.0.0
ms.assetid: CD9803F0-3DBE-4056-9E85-A834AD91D390
---

# New-CMAlertSubscription

## SYNOPSIS
Creates an alert subscription object.

## SYNTAX

```
New-CMAlertSubscription -Name <String> [-AlertId <Int32[]>] -EmailAddress <String[]> [-LocaleId <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAlertSubscription** cmdlet creates a subscription that sends alert notifications to one or more users when specific events occur in Microsoft System Center Configuration Manager.
Before you create an alert subscription, make sure that you have configured email settings for sending alert notifications, and that you have at least one alert configured in System Center Configuration Manager.

## EXAMPLES

### Example 1: Create an alert subscription
```
PS C:\>New-CMAlertSubscription -Name "Subscription01" -EmailAddress "evan.narvaez@contoso.com" -LocaleId 1033 -AlertIds 16777219
```

This command creates an alert subscription named Subscription01.
If there is an event that pertains to the specified alert, this subscription sends alert notifications to an email recipient.
Because the command specifies a locale ID of 1033, the subscription uses US English.

## PARAMETERS

### -AlertId
Specifies an array of alert identifiers for the subscription.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: AlertIds

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
Specifies an email address where you want to send an alert notification.
For example, david.chew@contoso.com.
You can separate multiple email addresses by using a semicolon.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: EmailAddresses

Required: True
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

### -LocaleId
Specifies a locale for alert messages.
For more information and a list of locale identifiers, see the Locale IDs Assigned by Microsoft topic at http://go.microsoft.com/fwlink/?LinkId=262651.

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

### -Name
Specifies the name of an alert subscription object.

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

[Get-CMAlertSubscription](./Get-CMAlertSubscription.md)

[Set-CMAlertSubscription](./Set-CMAlertSubscription.md)

[Remove-CMAlertSubscription](./Remove-CMAlertSubscription.md)


