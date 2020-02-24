---
author: aczechowski
description: Gets an object that represents a Configuration Manager database.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMDatabaseProperty
titleSuffix: Configuration Manager
---

# Get-CMDatabaseProperty

## SYNOPSIS
Gets an object that represents a Configuration Manager database.

## SYNTAX

```
Get-CMDatabaseProperty [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDatabaseProperty** cmdlet gets an object that represents a Microsoft System Center Configuration Manager database.
Use the site code for a site to specify a database.

When this cmdlet returns a database object in the console, it displays current settings for data compression, Broker port for the computer that runs Microsoft SQL Server, and the length of time that the database keeps data.
You can use the [Set-CMDatabaseProperty](Set-CMDatabaseProperty.md) cmdlet to change these values.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a database property
```
PS XYZ:\> Get-CMDatabaseProperty -SiteCode "CM2"
Key                                     Value
---                                     -----
SQL Server Service Broker Port          80
Retention Period                        10
IsCompression                           0
```

This command gets the database property for the site that has the site code CM2.

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

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

[Set-CMDatabaseProperty](Set-CMDatabaseProperty.md)
