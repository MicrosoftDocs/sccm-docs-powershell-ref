---
external help file: AdminUI.PS.DatabaseReplication.dll-Help.xml
ms.assetid: CC332293-14EF-4E4A-8F5B-0D16FD9EA33D
online version: https://go.microsoft.com/fwlink/?linkid=834299
schema: 2.0.0
---

# Get-CMDatabaseReplicationLinkProperty

## SYNOPSIS
Gets a replication link between a Configuration Manager parent site and child site.

## SYNTAX

```
Get-CMDatabaseReplicationLinkProperty -ParentSiteCode <String> -ChildSiteCode <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDatabaseReplicationLinkProperty** cmdlet gets a specified replication link between a Microsoft System Center Configuration Manager parent site and child site.

Database replication for Configuration Manager sites transfers data and merges changes made in a site database with information stored at other sites in the Configuration Manager hierarchy.
This enables all sites to share the same information.

## EXAMPLES

### Example 1: Get a replication link
```
PS C:\> Get-CMDatabaseReplicationLinkProperty -ChildSiteCode "CM8" -ParentSiteCode "CM1"
```

This command gets a replication link between specified parent and child sites.
You must specify both sites.

## PARAMETERS

### -ChildSiteCode
Specifies a site code for a Configuration Manager site.
This parameter refers to the child site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Site2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ParentSiteCode
Specifies a site code for a Configuration Manager site.
This parameter refers to the parent site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Site1

Required: True
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

[Set-CMDatabaseReplicationLinkProperty](./Set-CMDatabaseReplicationLinkProperty.md)


