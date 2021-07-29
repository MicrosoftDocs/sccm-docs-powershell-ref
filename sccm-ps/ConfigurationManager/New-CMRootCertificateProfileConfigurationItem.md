---
description: Create a root certificate profile.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/30/2020
schema: 2.0.0
title: New-CMRootCertificateProfileConfigurationItem
---

# New-CMRootCertificateProfileConfigurationItem

## SYNOPSIS

Create a root certificate profile.

## SYNTAX

```
New-CMRootCertificateProfileConfigurationItem -Path <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMRootCertificateProfileConfigurationItem** cmdlet creates a root certificate profile.
Client computers use root certificate profiles to chain their certificates back to a public key infrastructure (PKI) certification authority (CA).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a trusted root certificate profile configuration item

This command creates a trusted root certificate profile configuration item by using the digest file `C:\Digests\TrustedRootCertificate.xml`.

```powershell
New-CMRootCertificateProfileConfigurationItem -Path "C:\Digests\TrustedRootCertificate.xml"
```

## PARAMETERS

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

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

### -Path

Specify the path to the certificate digest file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DesiredConfigurationDigestPath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### IResultObject#SMS_ConfigurationPolicy
## NOTES

Cmdlet aliases: **New-CMTrustedRootCertificateProfileConfigurationItem**

## RELATED LINKS
