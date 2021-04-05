---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMNoOverwritePolicy

## SYNOPSIS

Create a policy to control computer restart performance at the risk of exposing BitLocker secrets.

## SYNTAX

```
New-CMNoOverwritePolicy [-PolicyState <State>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Create a policy to control computer restart performance at the risk of exposing BitLocker secrets. BitLocker secrets include key material used to encrypt data. This policy applies only when you enable BitLocker protection.

## EXAMPLES

### Example 1: New default enabled policy

This example creates a policy that's not configured.

```powershell
New-CMNoOverwritePolicy -PolicyState NotConfigured
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

- `Enabled`: If you enable this policy, memory isn't overwritten when the computer restarts. Preventing memory overwrite may improve restart performance, but it increases the risk of exposing BitLocker secrets.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, BitLocker secrets are removed from memory when the computer restarts.

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

### System.Object
## NOTES

## RELATED LINKS

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#prevent-memory-overwrite-on-restart)
