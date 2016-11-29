---
external help file: AdminUI.PS.Certificates.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834161
schema: 2.0.0
ms.assetid: 20865371-37E6-4090-9921-E2051D26D873
---

# Get-CMCertificate

## SYNOPSIS

## SYNTAX

```
Get-CMCertificate [-Id <String>] [-Thumbprint <String>] [-CertificateType <CertificateType>]
 [-KeyType <KeyType>] [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

### -CertificateType
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

### -Id
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


