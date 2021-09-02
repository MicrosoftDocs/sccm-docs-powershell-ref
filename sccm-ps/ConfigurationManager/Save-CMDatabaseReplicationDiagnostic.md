---
description: Saves database replication diagnostic information for Configuration Manager in a file.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Save-CMDatabaseReplicationDiagnostic
---

# Save-CMDatabaseReplicationDiagnostic

## SYNOPSIS
Saves database replication diagnostic information for Configuration Manager in a file.

## SYNTAX

```
Save-CMDatabaseReplicationDiagnostic -ChildSiteCode <String> [-FileName <String>] [-PassThru]
 [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Save-CMDatabaseReplicationDiagnostic** cmdlet saves diagnostic information for database replication issues for Configuration Manager in a specified file.
This cmdlet runs diagnostics for a link between a parent and a child site databases.
You can specify sites by either name or site code, but you cannot specify one site by name and the other by site code.

Configuration Manager database replication transfers data and merges changes made in a site database with the information stored in other sites in the Configuration Manager site hierarchy so that all sites share the same information.
Configuration Manager configures database replication automatically between a parent and child site.
Diagnostics identify problems in database replication.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Save database replication diagnostic
```
PS XYZ:\> Save-CMDatabaseReplicationDiagnostic -ChildSiteCode "CC2" -FileName "D:\Diagnostics\CCB_CC2_Diagnostics.csv" -ParentSiteCode "CCB"
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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.String
## NOTES

## RELATED LINKS

[Get-CMDatabaseReplicationLinkProperty](Get-CMDatabaseReplicationLinkProperty.md)

[Get-CMDataBaseReplicationStatus](Get-CMDataBaseReplicationStatus.md)


