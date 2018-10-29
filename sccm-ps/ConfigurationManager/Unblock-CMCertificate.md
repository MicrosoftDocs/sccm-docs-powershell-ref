---
external help file: AdminUI.PS.Certificates.dll-Help.xml
ms.assetid: CD441955-3619-4CCE-B1AA-E012BC7A6C99
online version: https://go.microsoft.com/fwlink/?linkid=834261
schema: 2.0.0
---

# Unblock-CMCertificate

## SYNOPSIS
Unblocks certificates.

## SYNTAX

### ByValue (Default)
```
Unblock-CMCertificate -Certificate <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Unblock-CMCertificate -Id <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Unblock-CMCertificate** cmdlet unblocks one or more public key infrastructure (PKI) certificates that Microsoft System Center Configuration Manager uses.

## EXAMPLES

### Example 1: Unblock a certificate
```
PS C:\>Unblock-CMCertificate -Id "BaseCert.txt"
```

This command unblocks the PKI certificate named BaseCert.

## PARAMETERS

### -Certificate
```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: InputObject

Required: True
Position: Named
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

### -Id
Specifies an array of IDs of certificates.

```yaml
Type: String
Parameter Sets: ById
Aliases: SMSID

Required: True
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

[Block-CMCertificate](Block-CMCertificate.md)

[Import-CMCertificate](Import-CMCertificate.md)

[Update-CMCertificate](Update-CMCertificate.md)


