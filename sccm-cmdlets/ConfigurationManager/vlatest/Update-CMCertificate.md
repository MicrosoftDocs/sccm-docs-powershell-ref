---
external help file: AdminUI.PS.Certificates.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834288
schema: 2.0.0
ms.assetid: EEFF1F3A-F8F1-4A3A-9AA7-D9687B6EC008
---

# Update-CMCertificate

## SYNOPSIS
Updates a certificate.

## SYNTAX

### ByValue (Default)
```
Update-CMCertificate -Path <String> -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Update-CMCertificate -Path <String> -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCertificate
```
Update-CMCertificate -InputObject <IResultObject> -X509Certificate <X509Certificate> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Update-CMCertificate** cmdlet updates a public key infrastructure (PKI) certificate that Microsoft System Center Configuration Manager uses.

## EXAMPLES

### Example 1: Update a certificate
```
PS C:\>Update-CMCertificate -Id "ManagementCertificate" -Path "C:\Certificates\Management.pfx"
```

This command modifies the certificate path for the certificate with the ID ManagementCertificate.
In this example, the path is changed to C:\Certificates\Management.pfx.

## PARAMETERS

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

### -Force
Forces the command to run without asking for user confirmation.

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
Parameter Sets: ById
Aliases: SmsId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: ByValue, ByCertificate
Aliases: Certificate

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path


```yaml
Type: String
Parameter Sets: ByValue, ById
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

### -X509Certificate


```yaml
Type: X509Certificate
Parameter Sets: ByCertificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Block-CMCertificate](./Block-CMCertificate.md)

[Unblock-CMCertificate](./Unblock-CMCertificate.md)

[Import-CMCertificate](./Import-CMCertificate.md)


