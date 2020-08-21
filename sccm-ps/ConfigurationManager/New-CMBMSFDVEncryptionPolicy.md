---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/13/2020
---

# New-CMBMSFDVEncryptionPolicy

## SYNOPSIS

Create a policy to manage whether to use BitLocker encryption on fixed data drives.

## SYNTAX

```
New-CMBMSFDVEncryptionPolicy [-PolicyState <State>] [-AutoUnlock <Dispensation>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to manage whether to use BitLocker encryption on fixed data drives.

When you enable this policy, also create a password policy for fixed data drives. The only exception is if you allow or require the use of auto-unlock for fixed data drives. For more information, see [New-CMFDVPassPhrasePolicy](New-CMFDVPassPhrasePolicy.md).

If you require the use of auto-unlock for fixed data drives, encrypt the OS volume too.

## EXAMPLES

### Example 1: New enabled policy that prohibits auto-unlock

This example creates a new policy that's enabled and doesn't allow auto-unlock.

```powershell
New-CMBMSFDVEncryptionPolicy -PolicyState Enabled -AutoUnlock Prohibit
```

## PARAMETERS

### -AutoUnlock

Allow, require, or prohibit BitLocker to automatically unlock any encrypted data drive. To use auto-unlock, also require BitLocker to encrypt the OS drive.

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

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy, the user has to put all fixed data drives under the BitLocker protection, and BitLocker encrypts the drives.

- `Disabled`: If you disable this policy, the user can't put fixed data drives under BitLocker protection. If you disable this policy after BitLocker encrypts fixed data drives, BitLocker decrypts the fixed data drives.

- `NotConfigured`: If you don't configure this policy, BitLocker doesn't require users to put fixed data drives under protection.

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

[New-CMFDVPassPhrasePolicy](New-CMFDVPassPhrasePolicy.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](https://docs.microsoft.com/mem/configmgr/protect/tech-ref/bitlocker/settings#fixed-data-drive-encryption)
