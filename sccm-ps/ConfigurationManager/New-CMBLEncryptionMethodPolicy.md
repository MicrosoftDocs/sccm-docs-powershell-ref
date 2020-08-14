---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/13/2020
---

# New-CMBLEncryptionMethodPolicy

## SYNOPSIS

Create a policy to configure the algorithm and cipher strength used by BitLocker Drive Encryption.

## SYNTAX

```
New-CMBLEncryptionMethodPolicy [-PolicyState <State>] [-EncryptionMethod <EncryptionMethod>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to configure the algorithm and cipher strength used by BitLocker Drive Encryption. This policy is applied when you turn on BitLocker. If the drive is already encrypted, or if encryption is in progress, changing the encryption method has no effect.

## EXAMPLES

### Example 1: New enabled policy with AES 256-bit encryption

This example creates a policy that's enabled and specifies AES 256-bit encryption.

```powershell
New-CMBLEncryptionMethodPolicy -PolicyState Enabled -EncryptionMethod AES256
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

### -EncryptionMethod

Specify one of the encryption methods for BitLocker to use when it encrypts drives. AES 128-bit (`Aes128`) is the default value.

```yaml
Type: EncryptionMethod
Parameter Sets: (All)
Aliases:
Accepted values: Aes128Diffuser, Aes256Diffuser, Aes128, Aes256

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

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy, use the **-EncryptionMethod** parameter to specify an encryption algorithm and key cipher strength. BitLocker uses these settings to encrypt drives.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, BitLocker uses the default encryption method of AES 128-bit.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.AdminConsole.BitlockerManagement.PolicyObject

## NOTES

## RELATED LINKS

[BitLocker settings reference](https://docs.microsoft.com/mem/configmgr/protect/tech-ref/bitlocker/settings#drive-encryption-method-and-cipher-strength)
