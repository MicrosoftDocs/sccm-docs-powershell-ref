---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/13/2020
---

# New-CMScCompliancePolicy

## SYNOPSIS

Create a compliance policy to associate an object identifier from a smart card certificate to a BitLocker-protected drive.

## SYNTAX

```
New-CMScCompliancePolicy [-PolicyState <State>] [-CertificateOid <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a compliance policy to associate an object identifier from a smart card certificate to a BitLocker-protected drive. The policy setting applies when you enable BitLocker on a device.

The object identifier is specified in the enhanced key usage (EKU) of a certificate. BitLocker identifies the certificates it can use to authenticate a user certificate to a BitLocker-protected drive. It matches the object identifier in the certificate with the object identifier that you define with this policy.​

The default object identifier is `1.3.6.1.4.1.311.67.1.1​`.

> [!NOTE]
> BitLocker doesn't require that a certificate have an EKU attribute. If the certificate has an EKU, set it to an object identifier (OID) that matches the OID that you configure for BitLocker.​

## EXAMPLES

### Example 1: New default enabled policy​

This example creates a new policy that's enabled and uses the default OID.

```powershell
New-CMScCompliancePolicy -PolicyState Enabled​
```

### Example 2: New enabled policy​ with a custom OID

This example creates a new policy that's enabled and uses a custom OID.

```powershell
New-CMScCompliancePolicy -PolicyState Enabled -CertificateOid "1.2.3.4.5.6.7.8.9"​
```

## PARAMETERS

### -CertificateOid

Use this parameter to specify a custom OID.

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

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy setting, use the **-CertificateOid** parameter to specify the object identifier that matches the object identifier in the smart card certificate.​

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy setting, it uses the default object identifier.

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
