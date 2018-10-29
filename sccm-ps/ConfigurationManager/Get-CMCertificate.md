---
external help file: AdminUI.PS.Certificates.dll-Help.xml
ms.assetid: 20865371-37E6-4090-9921-E2051D26D873
online version: https://go.microsoft.com/fwlink/?linkid=834161
schema: 2.0.0
---

# Get-CMCertificate

## SYNOPSIS
Gets a certificate.

## SYNTAX

```
Get-CMCertificate [-Id <String>] [-Thumbprint <String>] [-CertificateType <CertificateType>]
 [-KeyType <KeyType>] [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificate** cmdlet gets a certificate.

## EXAMPLES

### Example 1: Get all certificates
```
PS ABC:\> Get-CMCertificate
```

This command gets all certificates.

### Example 2: Get a certificate by ID and thumbprint
```
PS ABC:\> Get-CMCertificate -Id "{4680a1bb-ae51-4bdf-8f27-979eb49e444e}" -Thumbprint e1c2fff14282b61f79f78fbfca6721f0517ab767 -CertificateType DistributionPoint -KeyType SelfSigned
```

This command gets the self-signed distribution point certificate with the specified ID and thumbprint.

## PARAMETERS

### -CertificateType
Specifies the certificate type.
Valid values are:

- BootMedia
- DistributionPoint
- IsvProxy

```yaml
Type: CertificateType
Parameter Sets: (All)
Aliases: 
Accepted values: BootMedia, DistributionPoint, IsvProxy

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -Id
Specifies the ID of a certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmsId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
Specifies the key type of the certificate.
Valid values are:

- SelfSigned
- Issued

```yaml
Type: KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: SelfSigned, Issued

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Thumbprint
Specifies the thumbprint of the certificate.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Import-CMCertificate](Import-CMCertificate.md)

[Update-CMCertificate](Update-CMCertificate.md)

[Block-CMCertificate](Block-CMCertificate.md)

[Unblock-CMCertificate](Unblock-CMCertificate.md)
