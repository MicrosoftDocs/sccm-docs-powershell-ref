---
title: Get-CMIntuneSubscription
titleSuffix: Configuration Manager
description: Gets a Microsoft Intune subscription.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMIntuneSubscription

## SYNOPSIS
Gets a Microsoft Intune subscription.

## SYNTAX

```
Get-CMIntuneSubscription [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMIntuneSubscription** cmdlet gets the properties of a Microsoft Intune subscription in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get the Microsoft Intune subscription
```
PS C:\> Get-CMIntuneSubscription
```

This command gets the Microsoft Intune subscription for the Configuration Manager site.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject#SMS_CloudSubscription

## NOTES

## RELATED LINKS

[Add-CMIntuneSubscription](Add-CMIntuneSubscription.md)

[Remove-CMIntuneSubscription](Remove-CMIntuneSubscription.md)

[Set-CMIntuneSubscription](Set-CMIntuneSubscription.md)


