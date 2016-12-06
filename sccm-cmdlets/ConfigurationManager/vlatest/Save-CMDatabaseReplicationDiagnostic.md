---
external help file: AdminUI.PS.DatabaseReplication.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833582
schema: 2.0.0
ms.assetid: F80FD38D-B120-4F6B-9F6E-0DEC8A90A565
---

# Save-CMDatabaseReplicationDiagnostic

## SYNOPSIS
Saves database replication diagnostic information for Configuration Manager in a file.

## SYNTAX

```
Save-CMDatabaseReplicationDiagnostic [-SiteCode <String>] -ChildSiteCode <String> [-FileName <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Save-CMDatabaseReplicationDiagnostic** cmdlet saves diagnostic information for database replication issues for Microsoft System Center Configuration Manager in a specified file.
This cmdlet runs diagnostics for a link between a parent and a child site databases.
You can specify sites by either name or site code, but you cannot specify one site by name and the other by site code.

Configuration Manager database replication transfers data and merges changes made in a site database with the information stored in other sites in the Configuration Manager site hierarchy so that all sites share the same information.
Configuration Manager configures database replication automatically between a parent and child site.
Diagnostics identify problems in database replication.

## EXAMPLES

### Example 1: Save database replication diagnostic
```
PS C:\>Save-CMDatabaseReplicationDiagnostic -ChildSiteCode "CC2" -FileName "D:\Diagnostics\CCB_CC2_Diagnostics.csv" -ParentSiteCode "CCB"
```

This command saves database replication diagnostics in a file named CCB_CC2_Diagnostics.csv.
The command specifies a parent and child site by using site codes.

## PARAMETERS

### -ChildSiteCode
Specifies a site code for a Configuration Manager site.
This is the child site.

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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: False
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

### -FileName
Specifies a file name.
This cmdlet saves database diagnostic information for database replication to this file.

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

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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


```yaml
Type: String
Parameter Sets: (All)
Aliases: Site1, ParentSiteCode
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDatabaseReplicationLinkProperty](./Get-CMDatabaseReplicationLinkProperty.md)

[Get-CMDataBaseReplicationStatus](./Get-CMDataBaseReplicationStatus.md)


