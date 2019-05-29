---
title: New-CMExchangeServerConnectorPasswordSetting
titleSuffix: Configuration Manager
description: Adds new password settings to a Exchange Server connector in Configuration Manager.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# New-CMExchangeServerConnectorPasswordSetting

## SYNOPSIS
Adds new password settings to a Exchange Server connector in Configuration Manager.

## SYNTAX

```
New-CMExchangeServerConnectorPasswordSetting [-AllowSimplePassword <Boolean>] [-MaximumIdleTimeMins <Int32>]
 [-MinimumComplexChar <Int32>] [-MinimumPasswordLength <Int32>] [-PasswordComplexity <PasswordComplexityType>]
 -PasswordEnabled <Boolean> [-PasswordExpiration <Int32>] [-PasswordHistory <Int32>]
 [-PasswordRecovery <Boolean>] [-WipeAfterFailedAttempt <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServerConnectorPasswordSetting** cmdlet adds new password settings to a Microsoft Exchange Server connector in Microsoft System Center Configuration Manager.
An Exchange Server connector in Configuration Manager manages mobile devices that connect to an on-premise or online Exchange Server by using the Exchange ActiveSync protocol.

## EXAMPLES

### Example 1: Specify password settings for an Exchange Server connector
```
PS C:\> New-CMExchangeServerConnectorPasswordSetting -PasswordEnabled $True -MinimumPasswordLength 8 -PasswordExpiration 51 -PasswordHistory 21 -WipeAfterFailedAttempt 6 -MaximumIdleTimeMinutes 41 -PasswordComplexity Strong -MinimumComplexChar 3 -AllowSimplePassword $True -PasswordRecovery $True
```

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

## PARAMETERS

### -AllowSimplePassword
Indicates whether the mobile device can use simple numeric passwords.
A simple numeric password is one that has the same offset between each pair of digits.
For example, 2468 is a simple password because each pair of digits has an offset of two.
Simple numeric passwords can begin or end with 0 but cannot include values that wrap around in the middle of the digit string, such as 6802.

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
Specifies the minimum number of required complex characters in a device password.
A complex character is any character that is not a letter.

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
Specifies the minimum number of digits, characters, or both for the password.

The *PasswordEnabled* parameter must also have a value of $True for the *MinimumPasswordLength* parameter to take effect.
If *PasswordEnabled* has a value of $True, you can specify a minimum password length of between 1 and 40 characters.
If * PasswordEnabled* is $False, default password lengths apply: four characters for a simple password (*AllowSimplePassword* set to $True) or seven characters for an alphanumeric password (*PasswordComplexityType* set to $True).

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
Specifies the complexity type for the password.
Valid values are: 

- Pin: the password must be numeric. 
- Strong: the password must be alphanumeric.

The *PasswordEnabled* parameter must also have a value of $True for the *PasswordComplexity* parameter to take effect.

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
Indicates whether a user must set a password on the mobile device.

If this parameter is $True, the user must set a password.

If this parameter is $False, users can disable their password by using Control Panel and do not need to lock their Windows Mobile device.
However, the device does not inform the user that the password is disabled.

If you do not set a value for the parameter, the password-related settings on the mobile device remain in effect.

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
Specifies the number of days before the password expires and the user must enter a new one.

The *PasswordEnabled* parameter must also have a value of $True for the *PasswordExpiration* parameter to take effect.
If *PasswordExpiration* is set to $False, the user can keep the same password indefinitely.
If you do not set a value for *PasswordExpiration*, password expiration settings on the mobile device remain in effect.

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
Specifies the number of password changes a user must make before the user can reuse a previous password.

The *PasswordEnabled* parameter must also have a value of $True for the *PasswordHistory* parameter to take effect.
*PasswordExpiration* is set to $False, users can reuse any previous password.
If you do not set a value for *PasswordExpiration*, password settings on the mobile device remain in effect.

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
Indicates whether users can recover a missing device password or PIN from the mobile device.
If you do not set a value for this parameter, the password recovery options on the mobile device remain in effect.

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
Specifies the number of failed attempts to reset a password before the device wipes data from itself.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md)


