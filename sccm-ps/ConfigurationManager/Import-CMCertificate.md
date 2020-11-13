---
description: Imports a certificate.
external help file: AdminUI.PS.Certificates.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Import-CMCertificate
---

# Import-CMCertificate

## SYNOPSIS
Imports a certificate.

## SYNTAX

### ByValue (Default)
```
Import-CMCertificate [-PassThru] [-X509Certificate] <X509Certificate> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByFile
```
Import-CMCertificate [-PassThru] [-Path] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMCertificate** cmdlet imports a public key infrastructure (PKI) certificate to Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Import a certificate
```
PS XYZ:\>Import-CMCertificate -Path "\\Contoso01\CM\Certficates\BaseCert.txt"
```

This command imports the PKI certificate from the file named BaseCert.

## PARAMETERS

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

### -PassThru
Returns the current working object.
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
Specifies a certification path.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Security.Cryptography.X509Certificates.X509Certificate

## OUTPUTS

### IResultObject[]#SMS_ISVProxyCertificateInfo

### IResultObject#SMS_ISVProxyCertificateInfo

## NOTES

## RELATED LINKS

[Update-CMCertificate](Update-CMCertificate.md)

[Block-CMCertificate](Block-CMCertificate.md)

[Unblock-CMCertificate](Unblock-CMCertificate.md)


