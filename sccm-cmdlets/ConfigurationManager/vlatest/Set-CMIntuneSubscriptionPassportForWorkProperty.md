---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833894
schema: 2.0.0
ms.assetid: B62E719D-4285-49C7-803B-E5E4CEFECB45
---

# Set-CMIntuneSubscriptionPassportForWorkProperty

## SYNOPSIS
Updates a Microsoft Intune subscription to enable Windows Hello for business.

## SYNTAX

```
Set-CMIntuneSubscriptionPassportForWorkProperty [-Enable <Boolean>] [-RequireTpm <Boolean>]
 [-MinPinLength <Int32>] [-MaxPinLength <Int32>] [-AllowUppercase <Boolean>] [-AllowLowercase <Boolean>]
 [-AllowSpecialChar <Boolean>] [-PinExpirationDays <Int32>] [-PreventPinReuseCount <Int32>]
 [-EnableBiometrics <Boolean>] [-EnableEnhancedBiometrics <Boolean>] [-UseRemotePassport <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscriptionPassportForWorkProperty** updates the settings of a Microsoft Intune subscription to enable Windows Hello for business for enrolled devices.

NOTE: Windows Hello for Business was previously known as Microsoft Passport for Work.

## EXAMPLES

### Example 1: Enable Windows Hello for business
```
PS C:\>Set-CMIntuneSubscriptionPassportForWorkProperty -Enable $True -RequireTpm $True -MinPinLength 5 -MaxPinLength 8 -AllowUpperCase $True -AllowLowerCase $True -AllowSpecialChar $True -PinExpirationDays 2 -PreventPinReuseCount 3 -EnableBiometrics $False -EnableEnhancedBiometrics $False -UseRemotePassport $False
```

This command enables Windows Hello for business for enrolled devices.

## PARAMETERS

### -AllowLowercase
Indicates whether lower-case letters are allowed in the PIN.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RequireLowercase
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSpecialChar
Indicates whether special characters are allowed in the PIN.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RequireSpecialChar
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowUppercase
Indicates whether upper-case letters are allowed in the PIN.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RequireUppercase
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

### -Enable
Indicates whether Windows Hello for business for enrolled devices is enabled.

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

### -EnableBiometrics
Indicates whether biometric gestures is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableGestures
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEnhancedBiometrics
Indicates whether enhanced anti-spoofing is enabled, when available.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableEnhancedAntiSpoofing
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

### -MaxPinLength
Specifies the maximum required PIN length.

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

### -MinPinLength
Specifies the minimum required PIN length.

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

### -PassThru
Returns an object representing the item with which you are working.
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

### -PinExpirationDays
Specifies the number of days before the PIN expires.

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

### -PreventPinReuseCount
Specifies the number of previous PINs that the user is prevented from reusing.

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

### -RequireTpm
Indicates whether a Trusted Platform Module (TPM) is used.

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

### -UseRemotePassport
Indicates whether Phone Sign In is enabled.

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

[Set-CMIntuneSubscriptionAndroidProperty](./Set-CMIntuneSubscriptionAndroidProperty.md)

[Set-CMIntuneSubscriptionAppleDepProperty](./Set-CMIntuneSubscriptionAppleDepProperty.md)

[Set-CMIntuneSubscriptionAppleProperty](./Set-CMIntuneSubscriptionAppleProperty.md)

[Set-CMIntuneSubscriptionWindowsPhoneProperty](./Set-CMIntuneSubscriptionWindowsPhoneProperty.md)

[Set-CMIntuneSubscriptionWindowsProperty](./Set-CMIntuneSubscriptionWindowsProperty.md)
