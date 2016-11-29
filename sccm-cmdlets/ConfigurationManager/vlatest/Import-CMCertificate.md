---
external help file: AdminUI.PS.Certificates.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834040
schema: 2.0.0
ms.assetid: FECB6577-2499-441A-967F-FE505F41D1F7
---

# Import-CMCertificate

## SYNOPSIS
Imports a certificate.

## SYNTAX

### ByValue (Default)
```
Import-CMCertificate [-X509Certificate] <X509Certificate> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByFile
```
Import-CMCertificate [-Path] <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMCertificate** cmdlet imports a public key infrastructure (PKI) certificate to Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Import a certificate
```
PS C:\>Import-CMCertificate -Path "\\Contoso01\CM\Certficates\BaseCert.txt"
```

This command imports the PKI certificate from the file named BaseCert.

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

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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


```yaml
Type: String
Parameter Sets: ByFile
Aliases: 

Required: True
Position: 0
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
Parameter Sets: ByValue
Aliases: 

Required: True
Position: 0
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

[Update-CMCertificate](./Update-CMCertificate.md)

[Block-CMCertificate](./Block-CMCertificate.md)

[Unblock-CMCertificate](./Unblock-CMCertificate.md)


