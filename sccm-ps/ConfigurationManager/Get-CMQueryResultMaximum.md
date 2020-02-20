---
author: aczechowski
description: Gets the maximum number of rows that a Configuration Manager report query can return.
external help file: AdminUI.PS.Common.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMQueryResultMaximum
titleSuffix: Configuration Manager
---

# Get-CMQueryResultMaximum

## SYNOPSIS
Gets the maximum number of rows that a Configuration Manager report query can return.

## SYNTAX

```
Get-CMQueryResultMaximum [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMQueryResultMaximum** cmdlet gets the maximum number of rows that a Microsoft System Center Configuration Manager query can return.
By default, queries in Configuration Manager return only a subset of the matching rows in the database.
This cmdlet indicates the number of rows that Configuration Manager returns.
To change the maximum number of rows that a Configuration Manager query returns, use the [Set-CMQueryResultMaximum](Set-CMQueryResultMaximum.md) cmdlet.
By default, the maximum number of rows is unbound, which is different from the behavior of the Configuration Manager console, and is also different from earlier releases of the Configuration Manager cmdlet library.

## EXAMPLES

### Example 1: Get the report query result maximum
```
PS XYZ:\> Get-CMQueryResultMaximum
```

This command gets the maximum number of rows that a Configuration Manager report query can return.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMQueryResultMaximum](Set-CMQueryResultMaximum.md)


