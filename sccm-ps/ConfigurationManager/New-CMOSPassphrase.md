---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/13/2020
---

# New-CMOSPassphrase

## SYNOPSIS

Create a policy to specify the constraints for passwords used to unlock BitLocker-protected OS drives.

## SYNTAX

```
New-CMOSPassphrase [-PolicyState <State>] [-PasswordComplexity <Dispensation>] [-MinimumLength <UInt64>]
 [-RequireAsciiOnlyPassword] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to specify the constraints for passwords used to unlock BitLocker-protected OS drives. If you allow non-TPM protectors on OS drives, you can provision a password, enforce complexity requirements, and configure a minimum length. For these complexity requirement settings to be effective, also enable the group policy setting **Password must meet complexity requirements** in **Computer Configuration** > **Windows Settings** > **Security Settings** > **Account Policies** > **Password Policy**.

> [!NOTE]
> Windows enforces these settings when you enable BitLocker, not when it unlocks a volume. BitLocker allows a user to unlock a drive with any of the available protectors.
>
> You can't use passwords if you also enable Windows to use FIPS-compliant algorithms for encryption, hashing, and signing.

## EXAMPLES

### Example 1: New enabled policy that sets complexity and minimum length

This example creates a new policy that's enabled, requires a complex password that's at least 10 characters in length.

```powershell
New-CMOSPassphrase -PolicyState Enabled -PasswordComplexity Require -MinimumLength 10
```

### Example 2: New policy that requires ASCII

This example creates a policy that's enabled with the following properties:

- Allows but doesn't require a complex password
- At least 12 characters long
- Requires that the password only includes ASCII characters.

```powershell
New-CMOSPassphrase -PolicyState Enabled -PasswordComplexity Allow -MinimumLength 12 -RequireAsciiOnlyPassword
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

Use this parameter to configure password complexity for OS drives. To enforce complexity requirements on the password, set the value to `Require`.

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

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, the default length constraint of eight characters applies to OS drive passwords, and it doesn't check the password complexity.

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

### -RequireAsciiOnlyPassword

Add this parameter to require ASCII-only passwords for OS drives.

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

[BitLocker settings reference](https://docs.microsoft.com/mem/configmgr/protect/tech-ref/bitlocker/settings#operating-system-drive-password-policy)
