---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMUseFddEnforcePolicy

## SYNOPSIS

Create a policy to configure the number of days that fixed drives can remain noncompliant until they are forced to comply with BitLocker policies.

## SYNTAX

```
New-CMUseFddEnforcePolicy [-PolicyState <State>] [-GracePeriodDays <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to configure the number of days that fixed drives can remain noncompliant until they are forced to comply with BitLocker policies. After the grace period, users can't postpone the required action or request an exemption. The grace period starts when BitLocker determines the fixed data drive is noncompliant. BitLocker doesn't enforce the fixed data drive policy until the OS drive is compliant.

## EXAMPLES

### Example 1: New enabled policy with grace period set to seven days

This example creates a policy that's enabled and a grace period of one week (seven days).

```powershell
New-CMUseFddEnforcePolicy -PolicyState Enabled -GracePeriodDays 7
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

### -GracePeriodDays

Specify the number of days that a fixed data drive can be not protected by BitLocker. After this number of days, BitLocker protects the drive and encrypts it.

Specify a value of `0` to immediately enforce this fixed data drive policy after the OS drive becomes compliant.

```yaml
Type: Int32
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

- `Enabled`: If you enable this policy, BitLocker enforces the policy on fixed data drives, and provides users with grace period that you specify in the **-GracePeriodDays** parameter.

- `Disabled`, `NotConfigured`: If you disable or don't configure this setting, Configuration Manager doesn't require users to comply with BitLocker policies.

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

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#encryption-policy-enforcement-settings-fixed-data-drive)
