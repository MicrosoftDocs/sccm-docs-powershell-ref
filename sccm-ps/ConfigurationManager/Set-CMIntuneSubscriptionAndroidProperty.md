---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
ms.assetid: 14BD2A9D-635A-43C0-B477-B324BBB7FBC5
online version: https://go.microsoft.com/fwlink/?linkid=833883
schema: 2.0.0
---

# Set-CMIntuneSubscriptionAndroidProperty

## SYNOPSIS
Updates a Microsoft Intune subscription to enable Android enrollment.

## SYNTAX

```
Set-CMIntuneSubscriptionAndroidProperty [-Enable <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscriptionAndroidProperty** updates the settings of a Microsoft Intune subscription to enable Android enrollment.

## EXAMPLES

### Example 1: Enable Android enrollment
```
PS C:\> Set-CMIntuneSubscriptionAndroidProperty -Enable $True
```

This command enables Android enrollment for the Microsoft Intune subscription.

## PARAMETERS

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

[Set-CMIntuneSubscriptionAppleProperty](Set-CMIntuneSubscriptionAppleProperty.md)

[Set-CMIntuneSubscriptionAppleDepProperty](Set-CMIntuneSubscriptionAppleDepProperty.md)

[Set-CMIntuneSubscriptionPassportForWorkProperty](Set-CMIntuneSubscriptionPassportForWorkProperty.md)

[Set-CMIntuneSubscriptionWindowsPhoneProperty](Set-CMIntuneSubscriptionWindowsPhoneProperty.md)

[Set-CMIntuneSubscriptionWindowsProperty](Set-CMIntuneSubscriptionWindowsProperty.md)


