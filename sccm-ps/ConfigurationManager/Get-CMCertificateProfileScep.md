---
description: Gets a SCEP certificate profile.
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMCertificateProfileScep
---

# Get-CMCertificateProfileScep

## SYNOPSIS
Gets a SCEP certificate profile.

## SYNTAX

### ByValue (Default)
```
Get-CMCertificateProfileScep [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMCertificateProfileScep [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMCertificateProfileScep [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificateProfileScep** function gets a SCEP certificate profile.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a SCEP certificate profile by ID
```
PS XYZ:\> Get-CMcertificateProfileScep -Id 16777476
```

This command gets the SCEP certificate profile with the ID of 16777476.

### Example 2: Get a SCEP certificate profile by name
```
PS XYZ:\> Get-CMCertificateProfileScep -Name "TestSCEPProfile"
```

This command gets the SCEP certificate profile with the name TestSCEPProfile.

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
Specifies the CI_ID of a SCEP certificate profile.

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
Specifies the name of a SCEP certificate profile.

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

[New-CMCertificateProfileScep](New-CMCertificateProfileScep.md)

[Set-CMCertificateProfileScep](Set-CMCertificateProfileScep.md)


