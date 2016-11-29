---
external help file: AdminUI.PS.Migration.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833843
schema: 2.0.0
ms.assetid: 73184343-AC93-43B4-9C0A-EDBC23C5A950
---

# Clear-CMMigrationData

## SYNOPSIS
Deletes historical data about a data migration operation.

## SYNTAX

```
Clear-CMMigrationData -SourceSiteCode <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Clear-CMMigrationData** cmdlet deletes the historical data about a data migration operation.
With Microsoft System Center Configuration Manager, you can migrate data from a supported Configuration Manager hierarchy to a System Center Configuration Manager environment.
When you migrate data from a source hierarchy, you access data from the site databases that you identify in the source infrastructure and then transfer that data to your current environment from the database of the destination hierarchy.
**Clear-CMMigrationData** cleans up the historical data from the destination hierarchy database.

## EXAMPLES

### Example 1: Clean up historical data from a migration
```
PS C:\>Clear-CMMigrationData -SiteCode "C04"
```

This command removes the historical data from the destination site that has the site code C04.

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

[Set-CMMigrationExclusionList](./Set-CMMigrationExclusionList.md)

[Set-CMMigrationSource](./Set-CMMigrationSource.md)


