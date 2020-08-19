---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/18/2020
---

# New-CMRDVDenyWriteAccessPolicy

## SYNOPSIS

Create a policy to configure whether BitLocker protection is required for removable data drives to be writable on a computer.

## SYNTAX

```
New-CMRDVDenyWriteAccessPolicy [-PolicyState <State>] [-AllowWriteAccessToExternalOrganizationDrives]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to configure whether BitLocker protection is required for removable data drives to be writable on a computer.

## EXAMPLES

### Example 1: New default enabled policy

This example creates a new policy that's enabled

```powershell
New-CMRDVDenyWriteAccessPolicy -PolicyState Enabled
```

## PARAMETERS

### -AllowWriteAccessToExternalOrganizationDrives

Add this parameter to allow a removable data drive to be writeable without checking identification fields.

If you don't add this parameter, only drives with identification fields matching the computer's identification fields are writeable. When the system accesses a removable data drive, Windows checks for a valid identification field and allowed identification fields. These fields are defined by the "Provide the unique identifiers for your organization" policy setting. For more information, see [New-CMUidPolicy](New-CMUidPolicy.md).

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

- `Enabled`: If you enable this policy setting, Windows mounts all removable data drives that BitLocker doesn't protect as read-only. If BitLocker protects the drive, Windows mounts it with read and write access.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy setting, Windows mounts all removable data drives on the computer with read and write access.

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

[New-CMUidPolicy](New-CMUidPolicy.md)

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#deny-write-access-to-removable-drives-not-protected-by-bitlocker)
