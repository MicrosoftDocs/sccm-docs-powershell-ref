---
author: aczechowski
description: Gets a PFX certificate profile.
external help file: AdminUI.PS.Dcm-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMCertificateProfilePfx
titleSuffix: Configuration Manager
---

# Get-CMCertificateProfilePfx

## SYNOPSIS
Gets a PFX certificate profile.

## SYNTAX

### ByValue (Default)
```
Get-CMCertificateProfilePfx [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMCertificateProfilePfx [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMCertificateProfilePfx [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificateProfilePfx** function gets a PFX certificate profile.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a PFX certificate profile by name
```
PS XYZ:\> Get-CMCertificateProfilePfx -Name "Test1"
```

This command gets the PFX certificate profile object named Test1.

### Example 2: Get a PFX certificate profile by ID
```
PS XYZ:\> Get-CMcertificateprofilePfx -Id 16777499
```

This command gets the PFX certificate profile object with the ID of 16777499.

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
Specifies the ID of a PFX certificate profile.

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
Specifies the name of a PFX certificate profile.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMCertificateProfilePfx](New-CMCertificateProfilePfx.md)

[Set-CMCertificateProfilePfx](Set-CMCertificateProfilePfx.md)


