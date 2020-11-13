---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMFDVDenyWriteAccessPolicy

## SYNOPSIS

Create a new policy to determine whether BitLocker protection is required for fixed data drives to be writable on a computer.

## SYNTAX

```
New-CMFDVDenyWriteAccessPolicy [-PolicyState <State>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Create a new policy to determine whether BitLocker protection is required for fixed data drives to be writable on a computer.

## EXAMPLES

### Example 1: New default enabled policy

This example creates a new policy that's enabled.

```powershell
New-CMFDVDenyWriteAccessPolicy -PolicyState Enabled
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

- `Enabled`: If you enable this policy setting, Windows mounts all fixed data drives that BitLocker doesn't protect as read-only. If BitLocker protects the drive, Windows mounts it  with read and write access.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy setting, Windows mounts all fixed data drives on the computer with read and write access.

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

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#deny-write-access-to-fixed-drives-not-protected-by-bitlocker)
