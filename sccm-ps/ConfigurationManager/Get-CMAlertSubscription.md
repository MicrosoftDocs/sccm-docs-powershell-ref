---
description: Gets one or more alert subscription objects.
external help file: AdminUI.PS.Alerts.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Get-CMAlertSubscription
---

# Get-CMAlertSubscription

## SYNOPSIS
Gets one or more alert subscription objects.

## SYNTAX

### SearchByName (Default)
```
Get-CMAlertSubscription [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAlertSubscription -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAlertSubscription** cmdlet gets one or more Configuration Manager alert subscriptions and displays their properties.
If you specify the name or ID of an alert subscription, the cmdlet retrieves only that alert subscription.
If you specify part of the name or ID of an alert subscription, the cmdlet retrieves all alert subscriptions that match the partial name or ID.
If you do not specify anything, the cmdlet returns the properties of all alert subscriptions.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Display all alert subscriptions
```
PS XYZ:\> Get-CMAlertSubscription
```

This command displays all Configuration Manager alert subscriptions.

### Example 2: Display alert subscriptions by ID by using wildcard characters
```
PS XYZ:\> Get-CMAlertSubscription -Id 16777*
```

This command displays all Configuration Manager alert subscriptions that have an ID that starts with the number 16777.

### Example 3: Display an alert subscription by name
```
PS XYZ:\> Get-CMAlertSubscription -Name "Subscription01"
```

This command displays the Configuration Manager alert subscription named Subscription01.

## PARAMETERS

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

### -Id
Specifies the ID of a subscription.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of an alert subscription object.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_Subscription

### IResultObject#SMS_Subscription

## NOTES

## RELATED LINKS

[New-CMAlertSubscription](New-CMAlertSubscription.md)

[Set-CMAlertSubscription](Set-CMAlertSubscription.md)

[Remove-CMAlertSubscription](Remove-CMAlertSubscription.md)


