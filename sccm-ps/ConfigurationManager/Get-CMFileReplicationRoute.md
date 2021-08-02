---
description: Gets a file replication route from Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMFileReplicationRoute
---

# Get-CMFileReplicationRoute

## SYNOPSIS
Gets a file replication route from Configuration Manager.

## SYNTAX

### SearchBySiteCode (Default)
```
Get-CMFileReplicationRoute [-DestinationSiteCode <String>] [-SourceSiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySiteName
```
Get-CMFileReplicationRoute [-DestinationSiteName <String>] [-SourceSiteName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMFileReplicationRoute** cmdlet gets a file replication route from Configuration Manager.
Configuration Manager uses file replication routes to transfer file-based data between sites in a hierarchy.
Each file replication route identifies a destination site to which file-based data can transfer.

File replication were known as addresses in versions of Configuration Manager before Configuration Manager.
The functionality of file replication routes is the same as that of addresses in earlier versions.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a file replication route by using site codes
```
PS XYZ:\> Get-CMFileReplicationRoute -DestinationSiteCode "IM5" -SourceSiteCode "IM1"
```

This command creates a file replication route from the site that has the site code IM1 to the site that has the site code IM5.

## PARAMETERS

### -DestinationSiteCode
Specifies a destination site for data transfers by using a site code.

```yaml
Type: String
Parameter Sets: SearchBySiteCode
Aliases: DesSiteCode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationSiteName
Specifies a destination site for data transfers by using a site name.

```yaml
Type: String
Parameter Sets: SearchBySiteName
Aliases: DesSiteName

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

### -SourceSiteCode
Specifies a source site for data transfers by using a site code.

```yaml
Type: String
Parameter Sets: SearchBySiteCode
Aliases: SiteCode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceSiteName
Specifies a destination site for data transfers by using a site name.

```yaml
Type: String
Parameter Sets: SearchBySiteName
Aliases: SiteName

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

### IResultObject[]#SMS_SCI_Address
### IResultObject#SMS_SCI_Address
## NOTES

## RELATED LINKS

[New-CMFileReplicationRoute](New-CMFileReplicationRoute.md)

[Remove-CMFileReplicationRoute](Remove-CMFileReplicationRoute.md)

[Set-CMFileReplicationRoute](Set-CMFileReplicationRoute.md)


