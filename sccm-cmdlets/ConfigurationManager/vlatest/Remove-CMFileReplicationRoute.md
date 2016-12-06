---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834112
schema: 2.0.0
ms.assetid: 23EA2D57-BC59-4443-BF7B-817A956149A7
---

# Remove-CMFileReplicationRoute

## SYNOPSIS
Removes a file replication route from Configuration Manager.

## SYNTAX

```
Remove-CMFileReplicationRoute -SourceSiteCode <String> -DestinationSiteCode <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMFileReplicationRoute** cmdlet removes a file replication route from Microsoft System Center Configuration Manager.
System Center Configuration Manager uses file replication routes to transfer file-based data between sites in a hierarchy.
Each file replication route identifies a destination site to which file-based data can transfer.

File replication routes were known as addresses in versions of Configuration Manager before System Center Configuration Manager.
The functionality of file replication routes is the same as that of addresses in earlier versions.

## EXAMPLES

### Example 1: Remove a file replication route
```
PS C:\>Remove-CMFileReplicationRoute -DestinationSiteCode "IM5" -SourceSiteCode "IM1"
```

This command removes a file replication route from the site that has the site code IM1 to the site that has the site code IM5.

## PARAMETERS

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

### -DestinationSiteCode
Specifies the destination site code for the file replication route that you remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DesSiteCode
Required: True
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

### -Force
Forces the command to run without asking for user confirmation.

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

### -SourceSiteCode
Specifies the source site code for the file replication route that you remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SiteCode
Required: True
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

[Get-CMFileReplicationRoute](./Get-CMFileReplicationRoute.md)

[New-CMFileReplicationRoute](./New-CMFileReplicationRoute.md)

[Set-CMFileReplicationRoute](./Set-CMFileReplicationRoute.md)


