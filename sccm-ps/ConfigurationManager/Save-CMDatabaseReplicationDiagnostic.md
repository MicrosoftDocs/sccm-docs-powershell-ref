---
author: aczechowski
description: Saves database replication diagnostic information for Configuration Manager in a file.
external help file: AdminUI.PS.DatabaseReplication.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Save-CMDatabaseReplicationDiagnostic
titleSuffix: Configuration Manager
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

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

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

### -PassThru
Returns the current working object.
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDatabaseReplicationLinkProperty](Get-CMDatabaseReplicationLinkProperty.md)

[Get-CMDataBaseReplicationStatus](Get-CMDataBaseReplicationStatus.md)


