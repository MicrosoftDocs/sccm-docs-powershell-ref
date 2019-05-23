---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
ms.assetid: 346AC378-4A7D-4F06-BE42-EBB231762E27
online version: https://go.microsoft.com/fwlink/?linkid=833890
schema: 2.0.0
---

# Set-CMIntuneSubscriptionAppleProperty

## SYNOPSIS
Updates a Microsoft Intune subscription to enable iOS and Mac OS X (MDM) enrollment.

## SYNTAX

```
Set-CMIntuneSubscriptionAppleProperty [-Enable <Boolean>] [-ApnsCertificatePath <String>]
 [-ApnsCertificatePassword <SecureString>] [-CertificateExpiryAlertDays <Int32>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscriptionAppleProperty** cmdlet updates the settings of a Microsoft Intune subscription to enable iOS and Mac OS X (MDM) enrollment.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Enable iOS and Mac OS X (MDM) enrollment
```
PS XYZ:\> Set-CMIntuneSubscriptionAppleProperty -Enable $True -ApnsCertificatePath "C:\Certs\test.pem" -ApnsCertificatePassword $null -CertificateExpiryAlertDays 30
```

This command enables iOS and Mac OS X (MDM) enrollment for the Microsoft Intune subscription.

## PARAMETERS

### -ApnsCertificatePassword
Specifies, as a secure string, the password for the APNs certificate.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: CertificatePassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApnsCertificatePath
Specifies the path to the Apple Push Notification service (APNs) certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path, CertificatePath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateExpiryAlertDays
Specifies the number of days before the APNs certificate expires to show an alert.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ApnsCertificateExpiryAlertDays

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
Indicates whether iOS and Mac OS X (MDM) enrollment is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Enabled, EnableIosEnrollment, EnableMacEnrollment, EnableMdmEnrollment

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

[Set-CMIntuneSubscriptionAndroidProperty](Set-CMIntuneSubscriptionAndroidProperty.md)

[Set-CMIntuneSubscriptionAppleDepProperty](Set-CMIntuneSubscriptionAppleDepProperty.md)

[Set-CMIntuneSubscriptionPassportForWorkProperty](Set-CMIntuneSubscriptionPassportForWorkProperty.md)

[Set-CMIntuneSubscriptionWindowsPhoneProperty](Set-CMIntuneSubscriptionWindowsPhoneProperty.md)

[Set-CMIntuneSubscriptionWindowsProperty](Set-CMIntuneSubscriptionWindowsProperty.md)


