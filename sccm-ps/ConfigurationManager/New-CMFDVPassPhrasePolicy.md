---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMFDVPassPhrasePolicy

## SYNOPSIS

Create a policy to specify whether a password is required to unlock BitLocker-protected fixed data drives.

## SYNTAX

```
New-CMFDVPassPhrasePolicy [-PolicyState <State>] [-RequirePassword] [-PasswordComplexity <Dispensation>]
 [-MinimumLength <UInt64>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to specify whether a password is required to unlock BitLocker-protected fixed data drives. For these complexity requirement settings to be effective, also enable the group policy setting **Password must meet complexity requirements** in **Computer Configuration** > **Windows Settings** > **Security Settings** > **Account Policies** > **Password Policy**.

> [!NOTE]
> Windows enforces these settings when you enable BitLocker, not when it unlocks a volume. BitLocker allows a user to unlock a drive with any of the available protectors.
>
> You can't use passwords if you also enable Windows to use FIPS-compliant algorithms for encryption, hashing, and signing.

## EXAMPLES

### Example 1: New enabled policy that sets complexity and minimum length

This example creates a new policy that's enabled, requires a complex password that's at least 10 characters in length.

```powershell
New-CMFDVPassPhrasePolicy -PolicyState Enabled -PasswordComplexity Require -MinimumLength 10
```

### Example 2: New policy that requires a password

This example creates a policy that's enabled with the following properties:

- Allows but doesn't require a complex password
- At least 12 characters long
- Requires a password

```powershell
New-CMFDVPassPhrasePolicy -PolicyState Enabled -PasswordComplexity Allow -MinimumLength 12 -RequirePassword
```

## PARAMETERS

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

### -MinimumLength

Passwords must be at least `8` characters. To configure a greater minimum length for the password, use this parameter.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordComplexity

Use this parameter to configure password complexity for fixed data drives. To enforce complexity requirements on the password, set the value to `Require`.

- `Require`: When you enable BitLocker, a connection to a domain controller is necessary to validate the complexity of the password.

- `Allow`: The device tries to connect to a domain controller to validate the complexity. If it can't communicate with a domain controller, it still accepts the password whatever the actual complexity. BitLocker encrypts the drive using that password as a protector.

- `Prohibit`: The client doesn't connect to a domain controller to validate the password complexity.

```yaml
Type: Dispensation
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Require, Prohibit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy, users can configure a password that meets the requirements you define. To enforce complexity requirements on the password, use `-PasswordComplexity Require`.

- `Disabled`: If you disable this policy, the user can't use a password.

- `NotConfigured`: If you don't configure this policy, BitLocker supports passwords for fixed data drives with the default settings. The default settings don't include password complexity requirements and require only eight characters.

```yaml
Type: State
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequirePassword

Add this parameter to require a password to unlock a BitLocker-protected fixed data drive.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.AdminConsole.BitlockerManagement.PolicyObject

## NOTES

## RELATED LINKS

[New-CMBMSFDVEncryptionPolicy](New-CMBMSFDVEncryptionPolicy.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#fixed-data-drive-password-policy)
