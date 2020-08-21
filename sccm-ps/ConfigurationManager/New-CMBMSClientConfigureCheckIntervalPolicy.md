---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/13/2020
---

# New-CMBMSClientConfigureCheckIntervalPolicy

## SYNOPSIS

Create a policy to manage the key recovery service backup of BitLocker Drive Encryption recovery information.

## SYNTAX

```
New-CMBMSClientConfigureCheckIntervalPolicy [-PolicyState <State>] [-ClientWakeupFrequencyMinutes <Int32>]
 [-KeyRecoveryOption <KeyRecoveryOption>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Create a policy to manage the key recovery service backup of BitLocker Drive Encryption recovery information. This backup provides an administrative method of recovering data encrypted by BitLocker to prevent data loss because of lack of key information.

BitLocker recovery information includes the recovery password and some unique identifier data. You can also select to include a package that contains a BitLocker protected drive's encryption key. This key package is secured by one or more recovery passwords. The package may help with specialized recovery when the disk is damaged or corrupted.

This policy manages how often the client checks the BitLocker protection policies and status on the device. You can also manage the compliance and status information to save to the BitLocker report server. This behavior provides an administrative method of generating a compliance and status report.

## EXAMPLES

### Example 1: New policy with a 45-minute client check period and only password escrow

This example creates a policy that's enabled with the following attributes:

- The client reports compliance and status information to the BitLocker report service every 45 minutes.
- The client only sends the recovery password.

```powershell
New-CMBMSClientConfigureCheckIntervalPolicy -PolicyState Enabled -ClientWakeupFrequencyMinutes 45 -KeyRecoveryOption PasswordOnly
```

### Example 2: New policy with a daily client check period and escrows a recovery package

This example creates a policy that's enabled with the following attributes:

- The client reports compliance and status information to the BitLocker report service every 1440 minutes (one day).
- The client sends a recovery package with the password.

```powershell
New-CMBMSClientConfigureCheckIntervalPolicy -PolicyState Enabled -ClientWakeupFrequencyMinutes 1440 -KeyRecoveryOption PasswordAndPackage
```

## PARAMETERS

### -ClientWakeupFrequencyMinutes

Set this parameter to manage the frequency of the compliance and status information that the client reports to the BitLocker report service. The frequency is every 1 minute to 2880 minutes (48 hours). The default for the client to check status is 90 minutes.

Frequency values smaller than the default will increase network and server usage. Smaller values can limit the number of clients that the server can process.

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

### -KeyRecoveryOption

BitLocker recovery information includes the recovery password and some unique identifier data. You can also select to include a package that contains a BitLocker protected drive's encryption key. This key package is secured by one or more recovery passwords. The package may help with specialized recovery when the disk is damaged or corrupted.

```yaml
Type: KeyRecoveryOption
Parameter Sets: (All)
Aliases:
Accepted values: PasswordAndPackage, PasswordOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy, key recovery info is automatically and silently backed up to the configured key recovery server location. A status report is automatically and silently sent to the configured report server location.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, the client doesn't save key recovery or status report information.

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

[New-CMRDVConfigureBDEPolicy](New-CMRDVConfigureBDEPolicy.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](https://docs.microsoft.com/mem/configmgr/protect/tech-ref/bitlocker/settings#bitlocker-management-services)
