---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833967
schema: 2.0.0
ms.assetid: 611213A2-DA3D-4A5C-8769-2E9B92EF1B7A
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
The **Get-CMTrustedRootCertificate** cmdlet gets a trusted root certificate for Microsoft System Center Configuration Manager.
For native mode communication, System Center Configuration Manager authenticates, encrypts, and signs communications based on public key infrastructure (PKI) keys that depend on trusted root certificate.
Devices that communicate by using certificates must have a root certificate in common.
Devices in your System Center Configuration Manager hierarchy might have different root certificates.
If so, install all necessary trusted root certificates.

Computers that run the Windows operating system, as well as many other devices, rely on some well-known third-party root certificates.
If you deploy your own PKI, install the required root certificate.

## EXAMPLES

### Example 1: Get a trusted root certificate
```
PS C:\>Get-CMTrustedRootCertificate -CertificationAuthorityServerName "ContosoCA.Contoso.com"
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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


