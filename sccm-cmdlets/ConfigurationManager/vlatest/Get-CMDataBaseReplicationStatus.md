---
external help file: AdminUI.PS.DatabaseReplication.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 5BB8ECD0-6FB0-4FCB-8966-8BB7FCC10E5B
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
The **Get-CMDatabaseReplicationStatus** cmdlet gets the status of the database replication link for a Microsoft System Center Configuration Manager parent/child site pair.
The cmdlet identifies the sites by site code.

You can specify just the site code or just the name for a parent or child and get all the database replication links for the specified site.

## EXAMPLES

### Example 1: Get status using site codes
```
PS C:\>Get-CMDataBaseReplicationStatus -ChildSiteCode "CCC" -ParentSiteCode "CCA"
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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


