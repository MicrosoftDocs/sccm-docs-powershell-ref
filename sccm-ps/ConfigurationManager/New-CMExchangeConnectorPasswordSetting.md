---
description: Add new password settings to a Exchange Server connector in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/30/2020
schema: 2.0.0
title: New-CMExchangeConnectorPasswordSetting
---

# New-CMExchangeConnectorPasswordSetting

## SYNOPSIS

Add new password settings to a Exchange Server connector in Configuration Manager.

## SYNTAX

```
New-CMExchangeConnectorPasswordSetting [-AllowSimplePassword <Boolean>] [-MaximumIdleTimeMins <Int32>]
 [-MinimumComplexChar <Int32>] [-MinimumPasswordLength <Int32>] [-PasswordComplexity <PasswordComplexityType>]
 -PasswordEnabled <Boolean> [-PasswordExpiration <Int32>] [-PasswordHistory <Int32>]
 [-PasswordRecovery <Boolean>] [-WipeAfterFailedAttempt <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMExchangeConnectorPasswordSetting** cmdlet adds new password settings to a Microsoft Exchange Server connector in Configuration Manager. An Exchange Server connector in Configuration Manager manages mobile devices that connect to an on-premise or online Exchange Server by using the Exchange ActiveSync protocol.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Specify password settings for an Exchange Server connector

This command sets these password-related options for an Exchange Server connector:

- Requires the user to set a password on the mobile device.
- Requires the password to have at least eight characters or digits.
- Causes the password to expire after 51 days.

- Requires 21 password changes before the user can reuse an earlier password.
- Wipes data from the mobile device after six failed attempts to change the password.
- Allows 41 minutes to elapse before the mobile device locks itself.
- Requires an alphanumeric password.
- Allows passwords to be simple.
- Allows users to recover missing passwords from the mobile device.

```powershell
New-CMExchangeConnectorPasswordSetting -PasswordEnabled $True -MinimumPasswordLength 8 -PasswordExpiration 51 -PasswordHistory 21 -WipeAfterFailedAttempt 6 -MaximumIdleTimeMinutes 41 -PasswordComplexity Strong -MinimumComplexChar 3 -AllowSimplePassword $True -PasswordRecovery $True
```

## PARAMETERS

### -AllowSimplePassword
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

### -MaximumIdleTimeMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumIdleTimeMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumComplexChar
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

### -MinimumPasswordLength
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

### -PasswordComplexity
```yaml
Type: PasswordComplexityType
Parameter Sets: (All)
Aliases:
Accepted values: Pin, Strong

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordEnabled
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordExpiration
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

### -PasswordHistory
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

### -PasswordRecovery
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

### -WipeAfterFailedAttempt
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.HS.ExchangeConnectorPasswordSetting
## NOTES

Cmdlet aliases: **New-CMExchangeServerConnectorPasswordSetting**

## RELATED LINKS

[New-CMExchangeConnectorEmailManagementSetting](New-CMExchangeConnectorEmailManagementSetting.md)

[New-CMExchangeConnectorSecuritySetting](New-CMExchangeConnectorSecuritySetting.md)
