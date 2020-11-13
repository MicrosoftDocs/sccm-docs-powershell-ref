---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMEnhancedPIN

## SYNOPSIS

Create a policy to configure whether BitLocker can use enhanced startup PINs.

## SYNTAX

```
New-CMEnhancedPIN [-PolicyState <State>] [-RequireAsciiOnlyPin] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to configure whether BitLocker can use enhanced startup PINs. Enhanced startup PINs permit the use of characters including uppercase and lowercase letters, symbols, numbers, and spaces. This policy setting is applied when you turn on BitLocker.

Not all computers support enhanced PINs in the pre-boot environment. Before you enable this policy, evaluate if your devices are compatible with it. Use the **-RequireAsciiOnlyPin** parameter to help make enhanced PINs more compatible with computers that limit the type or number of characters that you can enter in the pre-boot environment.

## EXAMPLES

### Example 1: New default enabled policy

This example creates a policy that's enabled to allow enhanced PINs for startup.

```powershell
New-CMEnhancedPIN -PolicyState Enabled
```

### Example 2: New enabled policy with ASCII-only PIN

This example creates a policy that's enabled but restricts PINs to the ASCII character set.

```powershell
New-CMEnhancedPIN -PolicyState Enabled -RequireAsciiOnlyPin
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

- `Enabled`: If you enable this policy, all new BitLocker startup PINs will be enhanced PINs.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, BitLocker won't use enhanced PINs.

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

### -RequireAsciiOnlyPin

Use this parameter to help make enhanced PINs more compatible with computers that limit the type or number of characters that you can enter in the pre-boot environment.

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

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#allow-enhanced-pins-for-startup)
