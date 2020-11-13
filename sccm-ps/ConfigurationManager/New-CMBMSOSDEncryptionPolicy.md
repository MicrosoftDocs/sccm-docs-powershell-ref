---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMBMSOSDEncryptionPolicy

## SYNOPSIS

Create a policy to manage whether to encrypt the OS drive with BitLocker.

## SYNTAX

```
New-CMBMSOSDEncryptionPolicy [-PolicyState <State>] [-RequireTpm] [-MinimumPinLength <UInt32>]
 [-Protector <TpmProtector>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a policy to manage whether to encrypt the OS drive with BitLocker.

If you want to use BitLocker on a computer without a [Trusted Platform Module (TPM)](https://docs.microsoft.com/windows/security/information-protection/tpm/trusted-platform-module-top-node), don't use the **-RequireTpm** parameter. In this mode, BitLocker requires a password when the device starts up. If you forget the password, use a BitLocker recovery option to access the drive.

On a computer with a compatible TPM, BitLocker can use two authentication methods when the device starts up. This behavior provides added protection for encrypted data. When the computer starts, it can use only the TPM for authentication, or it can also require the entry of a personal identification number (PIN).

> [!TIP]
> For higher security, when you enable devices with TPM + PIN protector, consider disabling the following group policy settings in **System** > **Power Management** > **Sleep Settings**:
>
> - Allow Standby States (S1-S3) When Sleeping (Plugged In)
>
> - Allow Standby States (S1-S3) When Sleeping (On Battery)

## EXAMPLES

### Example 1: Create a new policy that requires TPM with PIN

This example creates a new policy that's enabled with the following attributes:

- Requires a TPM
- Require a PIN with the TPM
- The PIN needs to be at least 16 numbers

```powershell
New-CMBMSOSDEncryptionPolicy -PolicyState Enabled -RequireTpm -MinimumPinLength 16 -Protector TpmAndPin
```

### Example 2: Create a new policy for TPM only

This example creates a new policy that's enabled and requires only a TPM.

```powershell
New-CMBMSOSDEncryptionPolicy -PolicyState Enabled -Protector TpmOnly
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

### -MinimumPinLength

If you require a PIN, this value is the shortest length the user can specify. The user enters this PIN when the computer boots to unlock the drive. By default, the minimum PIN length is `4`. Set a value from `4` to `20`.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy, the user has to put the OS drive under BitLocker protection, and it encrypts the drive.

- `Disabled`: If you disable this policy, the user can't put the OS drive under BitLocker protection. If you apply this policy after the OS drive is encrypted, BitLocker decrypts the drive.

- `NotConfigured`: If you don't configure this policy, then BitLocker isn't required on the OS drive.

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

### -Protector

Use this parameter to specify a protector for the OS drive:

- `TpmOnly`: Only use the TPM as a protector

- `TpmAndPin`: Use a PIN with the TPM

```yaml
Type: TpmProtector
Parameter Sets: (All)
Aliases:
Accepted values: TpmOnly, TpmAndPin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireTpm

Add this parameter to configure the policy to require the device to have a compatible TPM.

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

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](https://docs.microsoft.com/mem/configmgr/protect/tech-ref/bitlocker/settings#operating-system-drive-encryption-settings)
