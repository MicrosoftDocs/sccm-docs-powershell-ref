---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMBLEncryptionMethodWithXts

## SYNOPSIS

Create a policy to configure the algorithm and cipher strength used by BitLocker Drive Encryption on Windows 10 devices.

## SYNTAX

```
New-CMBLEncryptionMethodWithXts [-PolicyState <State>] [-OSDriveEncryptionMethod <WindowsTenEncryptionMethod>]
 [-FixedDriveEncryptionMethod <WindowsTenEncryptionMethod>]
 [-RemovableDriveEncryptionMethod <WindowsTenEncryptionMethod>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to configure the algorithm and cipher strength used by BitLocker Drive Encryption on Windows 10 devices. This policy is applied when you turn on BitLocker. If the drive is already encrypted, or if encryption is in progress, changing the encryption method has no effect.

For Windows 8.1 devices, use the [New-CMBLEncryptionMethodPolicy](New-CMBLEncryptionMethodPolicy.md) cmdlet.

## EXAMPLES

### Example 1: New disabled policy

This example creates a Windows 10 policy that's disabled. Since the general policy specified with the New-CMBLEncryptionMethodPolicy cmdlet specifies AES-256, BitLocker uses that same encryption method on all devices.

```powershell
New-CMBLEncryptionMethodPolicy -PolicyState Enabled -EncryptionMethod AES256
New-CMBLEncryptionMethodWithXts -PolicyState Disabled
```

### Example 2: New enabled policy with XTS-CBC 128-bit encryption

This example creates a policy that's enabled and specifies XTS-CBC 128-bit encryption on all drive types.

```powershell
New-CMBLEncryptionMethodWithXts -PolicyState Enabled -OSDriveEncryptionMethod AesCbc128 -FixedDriveEncryptionMethod AesCbc128 -RemovableDriveEncryptionMethod AesCbc128
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

### -FixedDriveEncryptionMethod

Specify an encryption method for fixed data drives.

```yaml
Type: WindowsTenEncryptionMethod
Parameter Sets: (All)
Aliases:
Accepted values: AesXts128, AesXts256, AesCbc128, AesCbc256

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

### -OSDriveEncryptionMethod

Specify an encryption method for the OS drive.

```yaml
Type: WindowsTenEncryptionMethod
Parameter Sets: (All)
Aliases:
Accepted values: AesXts128, AesXts256, AesCbc128, AesCbc256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy, separately configure an encryption algorithm and key cipher strength for fixed data drives, OS drives, and removable data drives. For fixed and OS drives, the XTS-AES algorithm is recommended. If you'll use a removable drive in a Windows 8.1 device, use AES-CBC 128-bit or AES-CBC 256-bit.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, BitLocker uses AES with the same bit strength as a policy that you specify with the [New-CMBLEncryptionMethodPolicy](New-CMBLEncryptionMethodPolicy.md) cmdlet. If you don't enable that policy, BitLocker uses the default encryption method of XTS-AES 128-bit.

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

### -RemovableDriveEncryptionMethod

Specify an encryption method for removable drives.

```yaml
Type: WindowsTenEncryptionMethod
Parameter Sets: (All)
Aliases:
Accepted values: AesXts128, AesXts256, AesCbc128, AesCbc256

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

[New-CMBLEncryptionMethodPolicy](New-CMBLEncryptionMethodPolicy.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](https://docs.microsoft.com/mem/configmgr/protect/tech-ref/bitlocker/settings#drive-encryption-method-and-cipher-strength)
