---
description: Gets a trusted CA certificate profile.
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMCertificateProfileTrustedRootCA
---

# Get-CMCertificateProfileTrustedRootCA

## SYNOPSIS
Gets a trusted CA certificate profile.

## SYNTAX

### ByValue (Default)
```
Get-CMCertificateProfileTrustedRootCA [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMCertificateProfileTrustedRootCA [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMCertificateProfileTrustedRootCA [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificateProfileTrustedRootCA** function gets a trusted CA certificate profile.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a trusted CA certificate profile by ID
```
PS XYZ:\> Get-CMCertificateProfileTrustedRootCA -Id 16777479
```

This command gets the trusted CA certificate profile with the ID 16777479.

### Example 2: Get a trusted CA certificate profile by name
```
PS XYZ:\> Get-CMCertificateProfileTrustedRootCA -Name "Test01" -Fast
```

This command gets the trusted CA certificate profile named Test01, but does not return lazy properties.

## PARAMETERS

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

### -Id
Specifies the ID of a trusted CA certificate profile.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a trusted CA certificate profile.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMCertificateProfileTrustedRootCA](New-CMCertificateProfileTrustedRootCA.md)

[Set-CMCertificateProfileTrustedRootCA](Set-CMCertificateProfileTrustedRootCA.md)


