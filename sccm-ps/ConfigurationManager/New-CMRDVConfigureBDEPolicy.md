---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMRDVConfigureBDEPolicy

## SYNOPSIS

Create a policy to control the use of BitLocker on removable data drives.

## SYNTAX

```
New-CMRDVConfigureBDEPolicy [-PolicyState <State>] [-PreventEncryption] [-PreventSuspendAndDecrypt]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to control the use of BitLocker on removable data drives. This policy setting is applied when you turn on BitLocker.

After BitLocker encrypts a removable data drive, it saves recovery information based on the policy that you set with the [New-CMBMSClientConfigureCheckIntervalPolicy](New-CMBMSClientConfigureCheckIntervalPolicy.md) cmdlet.

When you enable BitLocker protection on a removable drive:

- Create a password policy for removable data drives. For more information, see [New-CMRDVPassPhrasePolicy](New-CMRDVPassPhrasePolicy.md).

- For higher security, disable the following user and computer group policies under **System** > **Removable Storage Access**:

  - **All Removable storage classes: Deny all access**

  - **Removable Disks: Deny write access**

  - **Removable Disks: Deny read access**

## EXAMPLES

### Example 1: New policy that prevents encryption and decryption of removable drives

This example creates a new policy that's enabled with the following attributes:

- Prevent users from applying BitLocker protection on removable data drives

- Prevent users from suspending or decrypting BitLocker on removable data drives

```powershell
New-CMRDVConfigureBDEPolicy -PolicyState Enabled -PreventEncryption -PreventSuspendAndDecrypt
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

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: When you enable this policy, you control how users can configure BitLocker.

- `NotConfigured`: If you don't configure this policy, users can use BitLocker on removable disk drives.

- `Disabled`: If you disable this policy, users can't use BitLocker on removable disk drives.

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

### -PreventEncryption

Add this parameter to prevent the user from running the BitLocker setup wizard on a removable data drive.

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

### -PreventSuspendAndDecrypt

Add this parameter to prevent the user from removing BitLocker Drive encryption from the drive. They also can't suspend BitLocker encryption during system maintenance.

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

[New-CMBMSClientConfigureCheckIntervalPolicy](New-CMBMSClientConfigureCheckIntervalPolicy.md)

[New-CMRDVPassPhrasePolicy](New-CMRDVPassPhrasePolicy.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](https://docs.microsoft.com/mem/configmgr/protect/tech-ref/bitlocker/settings#removable-data-drive-encryption)
