---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833840
schema: 2.0.0
ms.assetid: 5887137C-3DB1-4DBC-BD1D-9A751813E992
---

# New-CMWiredProfileObject

## SYNOPSIS
Creates a profile that specifies settings for AMT-based computers on a wired network.

## SYNTAX

```
New-CMWiredProfileObject -TrustedRootCertificate <X509Certificate2>
 -ClientAuthenticationMethod <ClientAuthenticationMethodType> -ClientIssuingCertificationAuthority <String>
 -ClientCertificationAuthorityName <String> -ClientCertificateTemplate <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMWiredProfileObject** cmdlet creates a Microsoft System Center Configuration Manager profile that specifies settings that Intel Active Management Technology (AMT)-based computers use on a wired network.
These settings must match the configuration on your Remote Authentication Dial-In User Service (RADIUS) server.
System Center Configuration Manager cannot validate that these settings with your RADIUS server.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Create a profile for AMT-based computers on a wired network
```
PS XYZ:\> New-CMWiredProfileObject -ClientAuthenticationMethod EapTtlsMschapv2 -ClientCertificateTemplate "Contoso Wired User" -ClientCertificationAuthorityName "Contoso CA 1" -ClientIssuingCertificationAuthority "ContosoCA.Contoso.com" -TrustedRootCertificate "Contoso Root"
```

This command creates a profile for Intel Active Management Technology (AMT)-based computers on a wired network.
The command specifies security settings, such as the client authentication method and information necessary for certificates.
These settings must match the settings for the Remote Authentication Dial-In User Service (RADIUS) server.

## PARAMETERS

### -ClientAuthenticationMethod
Specifies the client authentication method configured on your RADIUS server.
The acceptable values for this parameter are:

- EapTls.
EAP-TLS.
- EapTtlsMschapv2.
EAP-TTLS/MSCHAPv2.
- Peapv0EapMschapv2.
PEAPv0/EAP-MSCHAPv2. 

The default authentication method is EAP-TLS.

```yaml
Type: ClientAuthenticationMethodType
Parameter Sets: (All)
Aliases: 
Accepted values: EapTls, EapTtlsMschapv2, Peapv0EapMschapv2
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientCertificateTemplate
Specifies a client certificate template.

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

### -ClientCertificationAuthorityName
Specifies a certification authority for the client.

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

### -ClientIssuingCertificationAuthority
Specifies an issuing certification authority for the client.

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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: False
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

### -TrustedRootCertificate
Specifies the trusted root certificate that the RADIUS server uses as its server authentication certificate.

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMWirelessProfileObject](New-CMWirelessProfileObject.md)


