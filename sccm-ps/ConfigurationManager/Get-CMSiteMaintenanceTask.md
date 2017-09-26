---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 3F2EAC38-7AA8-4DC7-BB4B-4F5C3D3A87BE
online version: https://go.microsoft.com/fwlink/?linkid=833870
schema: 2.0.0
---

# Get-CMSiteMaintenanceTask

## SYNOPSIS
Gets maintenance tasks in Configuration Manager.

## SYNTAX

```
Get-CMSiteMaintenanceTask [-MaintenanceTaskName <String>] [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSiteMaintenanceTask** cmdlet gets maintenance tasks in Microsoft System Center Configuration Manager.
A maintenance task is a task in System Center Configuration Manager that performs maintenance on sites and databases.

## EXAMPLES

### Example 1: Get a maintenance task
```
PS C:\> Get-CMSiteMaintenanceTask -SiteCode "CM1" -MaintenanceTaskName "Backup"
```

This command gets the maintenance task named Backup for the Configuration Manager site that has the site code CM1.

## PARAMETERS

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

### -MaintenanceTaskName
Specifies an array of names for maintenance tasks.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ItemName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSiteMaintenanceTask](Set-CMSiteMaintenanceTask.md)


