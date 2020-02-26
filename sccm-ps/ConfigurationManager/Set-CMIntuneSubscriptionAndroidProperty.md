---
description: Updates a Microsoft Intune subscription to enable Android enrollment.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMIntuneSubscriptionAndroidProperty
---

# Set-CMIntuneSubscriptionAndroidProperty

## SYNOPSIS
Updates a Microsoft Intune subscription to enable Android enrollment.

## SYNTAX

```
Set-CMIntuneSubscriptionAndroidProperty [-Enable <Boolean>] [-BlockPersonalDevice <Boolean>]
 [-PreventMinimumVersion <String>] [-PreventMaximumVersion <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscriptionAndroidProperty** updates the settings of a Microsoft Intune subscription to enable Android enrollment.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Enable Android enrollment
```
PS XYZ:\> Set-CMIntuneSubscriptionAndroidProperty -Enable $True
```

This command enables Android enrollment for the Microsoft Intune subscription.

## PARAMETERS

### -BlockPersonalDevice
{{ Fill BlockPersonalDevice Description }}

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

### -Enable
Indicates whether to enable Android enrollment.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Enabled

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

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -PreventMaximumVersion
{{ Fill PreventMaximumVersion Description }}

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

### -PreventMinimumVersion
{{ Fill PreventMinimumVersion Description }}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMIntuneSubscriptionAppleProperty](Set-CMIntuneSubscriptionAppleProperty.md)

[Set-CMIntuneSubscriptionAppleDepProperty](Set-CMIntuneSubscriptionAppleDepProperty.md)

[Set-CMIntuneSubscriptionPassportForWorkProperty](Set-CMIntuneSubscriptionPassportForWorkProperty.md)

[Set-CMIntuneSubscriptionWindowsPhoneProperty](Set-CMIntuneSubscriptionWindowsPhoneProperty.md)

[Set-CMIntuneSubscriptionWindowsProperty](Set-CMIntuneSubscriptionWindowsProperty.md)


