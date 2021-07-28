---
description: Gets an object that represents a Configuration Manager database.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDatabaseProperty
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
The **Get-CMDatabaseProperty** cmdlet gets an object that represents a Configuration Manager database.
Use the site code for a site to specify a database.

When this cmdlet returns a database object in the console, it displays current settings for data compression, Broker port for the computer that runs Microsoft SQL Server, and the length of time that the database keeps data.
You can use the [Set-CMDatabaseProperty](Set-CMDatabaseProperty.md) cmdlet to change these values.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### Dictionary<string, object>
## NOTES

## RELATED LINKS

[Set-CMDatabaseProperty](Set-CMDatabaseProperty.md)
