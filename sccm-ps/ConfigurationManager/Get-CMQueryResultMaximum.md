---
description: Gets the maximum number of rows that a Configuration Manager report query can return.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMQueryResultMaximum
---

# Get-CMQueryResultMaximum

## SYNOPSIS
Gets the maximum number of rows that a Configuration Manager report query can return.

## SYNTAX

```
Get-CMQueryResultMaximum [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMQueryResultMaximum** cmdlet gets the maximum number of rows that a Configuration Manager query can return.
By default, queries in Configuration Manager return only a subset of the matching rows in the database.
This cmdlet indicates the number of rows that Configuration Manager returns.
To change the maximum number of rows that a Configuration Manager query returns, use the [Set-CMQueryResultMaximum](Set-CMQueryResultMaximum.md) cmdlet.
By default, the maximum number of rows is unbound, which is different from the behavior of the Configuration Manager console, and is also different from earlier releases of the Configuration Manager cmdlet library.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

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

### None

## OUTPUTS

### System.Int32

## NOTES

## RELATED LINKS

[Set-CMQueryResultMaximum](Set-CMQueryResultMaximum.md)


