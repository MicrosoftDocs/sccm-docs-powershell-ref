---
author: aczechowski
description: Creates a root certificate profile.
external help file:
manager: dougeby
Module Name: AdminUI.PS.Dcm
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMTrustedRootCertificateProfileConfigurationItem
titleSuffix: Configuration Manager
---

# New-CMTrustedRootCertificateProfileConfigurationItem

## SYNOPSIS
Creates a root certificate profile.

## SYNTAX

## DESCRIPTION
The **New-CMTrustedRootCertificateProfileConfigurationItem** cmdlet creates a root certificate profile.
Client computers use root certificate profiles to chain their certificates back to a corporate public key infrastructure (PKI) certification authority.

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

## OUTPUTS

## NOTES

## RELATED LINKS
