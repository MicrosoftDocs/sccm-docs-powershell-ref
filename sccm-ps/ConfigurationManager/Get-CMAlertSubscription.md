---
title: Get-CMAlertSubscription
titleSuffix: Configuration Manager
description: Gets one or more alert subscription objects.
ms.date: 05/01/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
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
The **Get-CMAlertSubscription** cmdlet gets one or more Microsoft System Center Configuration Manager alert subscriptions and displays their properties.
If you specify the name or ID of an alert subscription, the cmdlet retrieves only that alert subscription.
If you specify part of the name or ID of an alert subscription, the cmdlet retrieves all alert subscriptions that match the partial name or ID.
If you do not specify anything, the cmdlet returns the properties of all alert subscriptions.

## EXAMPLES

### Example 1: Display all alert subscriptions
```
PS C:\> Get-CMAlertSubscription
```

This command displays all System Center Configuration Manager alert subscriptions.

### Example 2: Display alert subscriptions by ID by using wildcard characters
```
PS C:\> Get-CMAlertSubscription -Id 16777*
```

This command displays all System Center Configuration Manager alert subscriptions that have an ID that starts with the number 16777.

### Example 3: Display an alert subscription by name
```
PS C:\> Get-CMAlertSubscription -Name "Subscription01"
```

This command displays the System Center Configuration Manager alert subscription named Subscription01.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMAlertSubscription](New-CMAlertSubscription.md)

[Set-CMAlertSubscription](Set-CMAlertSubscription.md)

[Remove-CMAlertSubscription](Remove-CMAlertSubscription.md)


