---
description: Creates an alert subscription object.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMAlertSubscription
---

# New-CMAlertSubscription

## SYNOPSIS
Creates an alert subscription object.

## SYNTAX

```
New-CMAlertSubscription -AddEmailAddress <String[]> [-AlertId <Int32[]>] [-LocaleId <Int32>] -Name <String>
 [-RequireValidLocaleId] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAlertSubscription** cmdlet creates a subscription that sends alert notifications to one or more users when specific events occur in Configuration Manager.
Before you create an alert subscription, make sure that you have configured email settings for sending alert notifications, and that you have at least one alert configured in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create an alert subscription
```
PS XYZ:\> New-CMAlertSubscription -Name "Subscription01" -EmailAddress "evan.narvaez@contoso.com" -LocaleId 1033 -AlertIds 16777219
```

This command creates an alert subscription named Subscription01.
If there is an event that pertains to the specified alert, this subscription sends alert notifications to an email recipient.
Because the command specifies a locale ID of 1033, the subscription uses US English.

## PARAMETERS

### -AddEmailAddress
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: EmailAddresses, EmailAddress, AddEmailAddresses

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -LocaleId
Specifies a locale for alert messages.
For more information and a list of locale identifiers, see [Appendix A: Product Behavior](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

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

### -RequireValidLocaleId
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

### None

## OUTPUTS

### IResultObject#SMS_Subscription

## NOTES

## RELATED LINKS

[Get-CMAlertSubscription](Get-CMAlertSubscription.md)

[Set-CMAlertSubscription](Set-CMAlertSubscription.md)

[Remove-CMAlertSubscription](Remove-CMAlertSubscription.md)


