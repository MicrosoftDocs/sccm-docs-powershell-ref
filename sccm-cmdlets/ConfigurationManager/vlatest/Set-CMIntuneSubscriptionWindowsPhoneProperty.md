---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
ms.assetid: E4CBCA72-31F0-40AC-B1AE-14EFA11F11F8
online version: https://go.microsoft.com/fwlink/?linkid=833897
schema: 2.0.0
---

# Set-CMIntuneSubscriptionWindowsPhoneProperty

## SYNOPSIS
Updates a Microsoft Intune subscription to enable Windows Phone enrollment.

## SYNTAX

```
Set-CMIntuneSubscriptionWindowsPhoneProperty [-EnableWindowsPhone8 <Boolean>] [-EnableWindowsPhone81 <Boolean>]
 [-AetTokenFilePath <String>] [-AetXmlFilePath <String>] [-PfxFilePath <String>]
 [-PfxFilePassword <SecureString>] [-NoToken] [-CertificateExpiryAlertDays <Int32>]
 [-CompanyPortalApplication <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscriptionWindowsPhoneProperty** updates the settings of a Microsoft Intune subscription to enable Windows Phone enrollment.

## EXAMPLES

### Example 1: Enable Windows Phone enrollment
```
PS C:\> Set-CMIntuneSubscriptionWindowsPhoneProperty -EnableWindowsPhone81 $True
```

This command enables Windows Phone 8.1 and Windows 10 Mobile enrollment for the Microsoft Intune subscription.

## PARAMETERS

### -AetTokenFilePath
Specifies the path to the application enrollment token (AET) file.

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

### -AetXmlFilePath
Specifies the path to the application enrollment token (AET) XML file.

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

### -CertificateExpiryAlertDays
Specifies the number of days before the Symantec certificate expires that an alert is shown.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SymantecCertificateExpiryAlertDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CompanyPortalApplication
Specifies the application package that contains the signed Company Portal .xap file.

```yaml
Type: IResultObject
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

### -EnableWindowsPhone8
Indicates whether Windows Phone 8.0 enrollment is enabled.

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

### -EnableWindowsPhone81
Indicates whether Windows Phone 8.1 and Windows 10 Mobile enrollment is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableWindowsMobile10

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

### -NoToken
Indicates that no application enrollment token is needed.

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

### -PfxFilePassword
Specifies, as a secure string, the password for the pfx certificate.

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

### -PfxFilePath
Specifies the path to a pfx certificate.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMIntuneSubscriptionAndroidProperty](./Set-CMIntuneSubscriptionAndroidProperty.md)

[Set-CMIntuneSubscriptionAppleDepProperty](./Set-CMIntuneSubscriptionAppleDepProperty.md)

[Set-CMIntuneSubscriptionAppleProperty](./Set-CMIntuneSubscriptionAppleProperty.md)

[Set-CMIntuneSubscriptionPassportForWorkProperty](./Set-CMIntuneSubscriptionPassportForWorkProperty.md)

[Set-CMIntuneSubscriptionWindowsProperty](./Set-CMIntuneSubscriptionWindowsProperty.md)


