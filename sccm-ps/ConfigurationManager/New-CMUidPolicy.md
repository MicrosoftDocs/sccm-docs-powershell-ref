---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMUidPolicy

## SYNOPSIS

Create a policy to associate unique organizational identifiers to a new drive that is enabled with BitLocker.

## SYNTAX

```
New-CMUidPolicy [-PolicyState <State>] [-BitLockerIdOid <Oid>] [-AllowedBitLockerIdOid <Oid>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a policy to associate unique organizational identifiers (OID) to a new drive that is enabled with BitLocker. These identifiers are stored as the identification field and allowed identification field. The identification field allows you to associate a unique organizational identifier to BitLocker-protected drives. This identifier is automatically added to new BitLocker-protected drives. You can update it on existing BitLocker-protected drives using the **Manage-BDE** command-line tool.

An identification field is required for management of certificate-based data recovery agents on BitLocker-protected drives and for potential updates to the BitLocker To Go Reader. BitLocker will only manage and update data recovery agents when the identification field on the drive matches the value configured in the identification field. In a similar manner, BitLocker will only update the BitLocker To Go Reader when the identification field on the drive matches the value configured for the identification field.

The allowed identification field is used in combination with the [New-CMRDVDenyWriteAccessPolicy](New-CMRDVDenyWriteAccessPolicy.md) cmdlet to help control the use of removable drives in your organization. It's a comma-separated list of identification fields from your organization or other external organizations.

When a BitLocker-protected drive is mounted on another BitLocker-enabled computer, the identification field and allowed identification field will be used to determine whether the drive is from an outside organization.

> [!NOTE]
> Identification fields are required for management of certificate-based data recovery agents on BitLocker-protected drives. BitLocker only manages and updates certificate-based data recovery agents when the identification field is present on a drive and is identical to the value configured on the computer. The identification field can be any value of 260 characters or fewer.

## EXAMPLES

### Example 1: New enabled policy with custom OIDs

This example creates a new policy that's enabled and sets custom IDs.

```powershell
New-CMUidPolicy -PolicyState Enabled -BitLockerIdOid "1.2.840.113549.1.1.1" -AllowedBitLockerIdOid "1.3.6.1.4.1.311.20.2"
```

## PARAMETERS

### -AllowedBitLockerIdOid

Specify a comma-separated list of allowed identifiers from your organization or other external organizations.

```yaml
Type: Oid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BitLockerIdOid

Specify the BitLocker identifier.

```yaml
Type: Oid
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

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy setting, you can configure the identification field on the BitLocker-protected drive and any allowed identification field used by your organization.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy setting, the identification field isn't required.

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

[New-CMRDVDenyWriteAccessPolicy](New-CMRDVDenyWriteAccessPolicy.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#organization-unique-identifiers)
