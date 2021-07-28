---
description: Gets the status for database replication.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDatabaseReplicationStatus
---

# Get-CMDatabaseReplicationStatus

## SYNOPSIS
Gets the status for database replication.

## SYNTAX

```
Get-CMDatabaseReplicationStatus [-ChildSiteCode <String>] [-ParentSiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDatabaseReplicationStatus** cmdlet gets the status of the database replication link for a Configuration Manager parent/child site pair.
The cmdlet identifies the sites by site code.

You can specify just the site code or just the name for a parent or child and get all the database replication links for the specified site.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get status using site codes
```
PS XYZ:\> Get-CMDataBaseReplicationStatus -ChildSiteCode "CCC" -ParentSiteCode "CCA"
```

This command gets the status of a database replication link for the child with a site code CCC and the parent with a site code CCA.

## PARAMETERS

### -ChildSiteCode
Specifies a site code for a child site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Site2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ParentSiteCode
Specifies a site code for a parent site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Site1

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

### IResultObject[]#SMS_ReplicationLinkSummary
### IResultObject#SMS_ReplicationLinkSummary
## NOTES

## RELATED LINKS
