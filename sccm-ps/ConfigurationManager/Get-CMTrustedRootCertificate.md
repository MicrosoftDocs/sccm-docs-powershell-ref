---
description: Gets a trusted root certificate for Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMTrustedRootCertificate
---

# Get-CMTrustedRootCertificate

## SYNOPSIS
Gets a trusted root certificate for Configuration Manager.

## SYNTAX

```
Get-CMTrustedRootCertificate [-CAServerName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMTrustedRootCertificate** cmdlet gets a trusted root certificate for Configuration Manager.
For native mode communication, Configuration Manager authenticates, encrypts, and signs communications based on public key infrastructure (PKI) keys that depend on trusted root certificate.
Devices that communicate by using certificates must have a root certificate in common.
Devices in your Configuration Manager hierarchy might have different root certificates.
If so, install all necessary trusted root certificates.

Computers that run the Windows operating system, as well as many other devices, rely on some well-known third-party root certificates.
If you deploy your own PKI, install the required root certificate.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a trusted root certificate
```
PS XYZ:\> Get-CMTrustedRootCertificate -CertificationAuthorityServerName "ContosoCA.Contoso.com"
```

This command gets a trusted root certificate from the internal server named ContosoCA.Contoso.com.

## PARAMETERS

### -CAServerName
```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificationAuthorityServerName

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
