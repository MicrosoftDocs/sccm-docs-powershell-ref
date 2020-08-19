---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/18/2020
---

# New-CMUseOsEnforcePolicy

## SYNOPSIS

Create a policy to configure the number of days that users can delay complying with BitLocker policies for their OS drive.

## SYNTAX

```
New-CMUseOsEnforcePolicy [-PolicyState <State>] [-GracePeriodDays <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to configure the number of days that users can delay complying with BitLocker policies for their OS drive. After the grace period expires, users can't postpone the required action or request an exemption. The grace period begins when BitLocker first detects that the OS drive is noncompliant. This grace period is the same for all users of the computer, regardless of when each user signs in.

## EXAMPLES

### Example 1: New enabled policy with a grace period of seven days

This example creates a policy that's enabled and a grace period of one week (five days).

```powershell
New-CMUseOsEnforcePolicy -PolicyState Enabled -GracePeriodDays 7
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

Specify the number of days that the OS drive can be not protected by BitLocker. After this number of days, BitLocker protects the drive and encrypts it.

Specify a value of `0` to immediately enforce this OS drive policy.

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

- `Enabled`: If you enable this policy, BitLocker enforces the policy on the OS drive, and provides users with grace period that you specify in the **-GracePeriodDays** parameter.

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

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#encryption-policy-enforcement-settings-os-drive)
