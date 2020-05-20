---
description: Creates a t s partition setting.
external help file:
Module Name: AdminUI.PS.Dcm
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMTSPartitionSetting
---

# New-CMTrustedRootCertificateProfileConfigurationItem

## SYNOPSIS
Creates a root certificate profile.

## SYNTAX

## DESCRIPTION
The **New-CMTrustedRootCertificateProfileConfigurationItem** cmdlet creates a root certificate profile.
Client computers use root certificate profiles to chain their certificates back to a corporate public key infrastructure (PKI) certification authority.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a trusted root certificate profile configuration item
```
PS XYZ:\> New-CMTrustedRootCertificateProfileConfigurationItem -DesiredConfigurationDigestPath "C:\Digests\TrustedRootCertificate.xml"
```

This command creates a trusted root certificate profile configuration item by using the digest file C:\Digests\TrustedRootCertificate.xml .

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS
