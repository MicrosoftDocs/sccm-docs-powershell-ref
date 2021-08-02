---
description: Get a Configuration Manager query.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2020
schema: 2.0.0
title: Get-CMQuery
---

# Get-CMQuery

## SYNOPSIS

Get a Configuration Manager query.

## SYNTAX

### ByName (Default)
```
Get-CMQuery [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMQuery [-Id <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a query from the Configuration Manager site. Configuration Manager queries define a WMI Query Language (WQL) expression to get information from the site database based on the criteria you provide. WQL is similar to SQL, but still goes through the SMS Provider instead of directly to the database. So WQL still abides by your role-based access configuration.

Queries can return most types of Configuration Manager objects, which include computers, sites, collections, applications, and inventory data. For more information, see [Introduction to queries in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-queries).

By default, Configuration Manager includes several queries. You can use this cmdlet to review the default queries.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This command returns all queries with the name containing "ConfigMgr clients".

```powershell
Get-CMQuery -Name "*ConfigMgr clients *"
```

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

### -Id

Specify the ID of the query to get. For example, `"XYZ00006"`.

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the query to get.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_Query
### IResultObject#SMS_Query
## NOTES

## RELATED LINKS

[Export-CMQuery](Export-CMQuery.md)
[Import-CMQuery](Import-CMQuery.md)
[Invoke-CMQuery](Invoke-CMQuery.md)
[New-CMQuery](New-CMQuery.md)
[Remove-CMQuery](Remove-CMQuery.md)
[Set-CMQuery](Set-CMQuery.md)
[Introduction to queries in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-queries)
