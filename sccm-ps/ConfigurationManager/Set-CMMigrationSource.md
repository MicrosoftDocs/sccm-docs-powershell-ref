---
description: Specifies or changes settings for a migration source site in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMMigrationSource
---

# Set-CMMigrationSource

## SYNOPSIS
Specifies or changes settings for a migration source site in Configuration Manager.

## SYNTAX

```
Set-CMMigrationSource [-EnableDistributionPointSharing <Boolean>] [-SmsProviderAccount <String>]
 -SourceSiteServerName <String> [-SqlServerAccount <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMMigrationSource** cmdlet specifies or changes settings for a migration source site in Configuration Manager.
To enable migration of data to your Configuration Manager environment, you must configure a supported Configuration Manager source hierarchy and specify one or more source sites that contain data that you want to migrate.

By default, the top-level site of the hierarchy becomes a source site of the source hierarchy.
If you migrate from a Configuration Manager 2007 hierarchy, you can configure additional source sites for migration.
If you migrate from a Configuration Manager hierarchy, you do not need to configure additional source sites because the Configuration Manager shared database at the top of the source hierarchy contains all of the information that you can migrate.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Specify a migration source
```
PS XYZ:\> Set-CMMigrationSource -SourceSiteServerName "cmdev-contoso01" -SmsProviderAccount "tsqa\pattifuller" -SqlServerAccount "tsqa\pattifuller" -EnableDistributionPointSharing $True
```

This command specifies the site server named cmdev-contoso01 as the source of migration data.
It uses the user account for tsqa\pattifuller to provide access to the SQL Server database at the top of the source hierarchy and to connect to the SMS provider and source site database for the source site.
The command also shares distribution points between the source and destination hierarchies.

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

### -EnableDistributionPointSharing
Indicates whether Configuration Manager shares distribution points between source and destination hierarchies.

```yaml
Type: Boolean
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

### -SmsProviderAccount
Specifies the name of the account that the top-level site in the destination hierarchy uses to connect to the SMS Provider and the site database of the source site.
The top-level site uses these connections to retrieve objects and distribution points.

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

### -SourceSiteServerName
Specifies the name of a server that contains a source site.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlServerAccount
Specifies a SQL Server account that provides access to the top-level SQL Server database in the source hierarchy.
The account must have read and run permissions for this database.

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

### System.Object
## NOTES

## RELATED LINKS

[Set-CMMigrationExclusionList](Set-CMMigrationExclusionList.md)

[Clear-CMMigrationData](Clear-CMMigrationData.md)


