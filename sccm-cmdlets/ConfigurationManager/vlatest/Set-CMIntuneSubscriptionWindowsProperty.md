---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 01422A54-9C29-45FD-9FED-34787A17C362
---

# Set-CMIntuneSubscriptionWindowsProperty

## SYNOPSIS
Updates a Microsoft Intune subscription to enable Windows enrollment.

## SYNTAX

```
Set-CMIntuneSubscriptionWindowsProperty [-Enable <Boolean>] [-CertificatePath <String>]
 [-CertificatePassword <SecureString>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscriptionWindowsProperty** cmdlet updates the settings of a Microsoft Intune subscription to enable Windows enrollment.

## EXAMPLES

### Example 1: Enable Windows enrollment
```
PS C:\>$SecPasswd = ConvertTo-SecureString "P@ssW0rD!" -AsPlainText -Force
PS C:\> Set-CMIntuneSubscriptionWindowsProperties -Enable $True -CertificatePath "C:\Certs\sign.pfx" -CertificatePassword $SecPasswd
```

This command enables Windows enrollment for the Microsoft Intune subscription.

## PARAMETERS

### -CertificatePassword
Specifies, as a secure string, the password for the code-signing certificate.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePath
Specifies the path to the code-signing certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CodeSigningCertificatePath

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
Indicates whether Windows enrollment is enabled.

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

[Set-CMIntuneSubscriptionPassportForWorkProperty](./Set-CMIntuneSubscriptionPassportForWorkProperty.md)

[Set-CMIntuneSubscriptionWindowsPhoneProperty](./Set-CMIntuneSubscriptionWindowsPhoneProperty.md)


