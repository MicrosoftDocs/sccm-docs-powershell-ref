---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/18/2020
---

# New-CMBlmSetting

## SYNOPSIS

Create a BitLocker management settings policy.

## SYNTAX

```
New-CMBlmSetting [-Policies <PolicyObject[]>] -Name <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a BitLocker management settings policy. You configure the specific policies with other cmdlets, and then use this cmdlet to create the management policy. For more information on the specific policy cmdlets, see [Related links](#related-links).

Use the [New-CMSettingDeployment](New-CMSettingDeployment.md) cmdlet to deploy this setting to a collection.

## EXAMPLES

### Example 1: Create a BitLocker setting with some standard policies

This example creates a new BitLocker management setting with a collection of standard BitLocker policies.

```powershell
$policies = @()

$policies += New-CMBLEncryptionMethodWithXts  -PolicyState Enabled -OSDriveEncryptionMethod AesXts256
$policies += New-CMBMSOSDEncryptionPolicy -PolicyState Enabled -Protector TpmOnly
$Policies += New-CMUseOsEnforcePolicy -PolicyState Enabled -GracePeriodDays 0
$Policies += New-CMBMSClientConfigureCheckIntervalPolicy -PolicyState Enabled -ClientWakeupFrequencyMinutes 9

New-CMBlmSetting -Name "BLM Settings" -Policies $policies
```

## PARAMETERS

### -Description

Specify an optional description to better identify this policy.

```yaml
Type: String
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

### -Name

Specify a name for this policy to identify it.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policies

Specify an array of BitLocker policies to include. For more information on the specific policy cmdlets, see [Related links](#related-links).

If you don't specify any policies with the **-Policies** parameter, the default policy is a single, not configured, OS drive encryption policy. For more information on this default policy type, see [New-CMBMSOSDEncryptionPolicy](New-CMBMSOSDEncryptionPolicy.md).

```yaml
Type: PolicyObject[]
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

### Microsoft.ConfigurationManagement.Cmdlets.BitLockerManagement.Commands.BlmSettings

## NOTES

## RELATED LINKS

[New-CMBLEncryptionMethodPolicy](New-CMBLEncryptionMethodPolicy.md)

[New-CMBLEncryptionMethodWithXts](New-CMBLEncryptionMethodWithXts.md)

[New-CMBMSClientConfigureCheckIntervalPolicy](New-CMBMSClientConfigureCheckIntervalPolicy.md)

[New-CMBMSFDVEncryptionPolicy](New-CMBMSFDVEncryptionPolicy.md)

[New-CMBMSOSDEncryptionPolicy](New-CMBMSOSDEncryptionPolicy.md)

[New-CMBMSUserExemptionPolicy](New-CMBMSUserExemptionPolicy.md)

[New-CMEnhancedPIN](New-CMEnhancedPIN.md)

[New-CMFDVDenyWriteAccessPolicy](New-CMFDVDenyWriteAccessPolicy.md)

[New-CMFDVPassPhrasePolicy](New-CMFDVPassPhrasePolicy.md)

[New-CMMoreInfoUrlPolicy](New-CMMoreInfoUrlPolicy.md)

[New-CMNoOverwritePolicy](New-CMNoOverwritePolicy.md)

[New-CMOSPassphrase](New-CMOSPassphrase.md)

[New-CMPrebootRecoveryInfo](New-CMPrebootRecoveryInfo.md)

[New-CMRDVConfigureBDEPolicy](New-CMRDVConfigureBDEPolicy.md)

[New-CMRDVDenyWriteAccessPolicy](New-CMRDVDenyWriteAccessPolicy.md)

[New-CMRDVPassPhrasePolicy](New-CMRDVPassPhrasePolicy.md)

[New-CMScCompliancePolicy](New-CMScCompliancePolicy.md)

[New-CMTpmAutoResealPolicy](New-CMTpmAutoResealPolicy.md)

[New-CMUidPolicy](New-CMUidPolicy.md)

[New-CMUseFddEnforcePolicy](New-CMUseFddEnforcePolicy.md)

[New-CMUseOsEnforcePolicy](New-CMUseOsEnforcePolicy.md)

[New-CMSettingDeployment](New-CMSettingDeployment.md)

[Deploy BitLocker management](/mem/configmgr/protect/deploy-use/bitlocker/deploy-management-agent)
