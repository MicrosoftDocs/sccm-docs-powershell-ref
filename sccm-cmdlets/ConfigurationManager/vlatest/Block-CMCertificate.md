---
external help file: AdminUI.PS.Certificates.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833819
schema: 2.0.0
ms.assetid: BB56BBF5-A38E-4BDE-B32B-EE42739B4945
---

# Block-CMCertificate

## SYNOPSIS
Blocks a certificate.

## SYNTAX

### ByValue (Default)
```
Block-CMCertificate [-InputObject] <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Block-CMCertificate [-Id] <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Block-CMCertificate** cmdlet blocks a certificate.
Microsoft System Center Configuration Manager uses certificates to manage boot media, Pre-Boot eXecution Environment (PXE) deployments, and Independent Software Vendors (ISV) proxies.

## EXAMPLES

### Example 1: Block a certificate
```
PS C:\>Block-CMCertificate -Id "11729"
```

This command blocks the certificate that has the specified ID.

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

### -Id
Specifies an array of certificate IDs.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: SmsId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

[Import-CMCertificate](./Import-CMCertificate.md)

[Unblock-CMCertificate](./Unblock-CMCertificate.md)

[Update-CMCertificate](./Update-CMCertificate.md)


