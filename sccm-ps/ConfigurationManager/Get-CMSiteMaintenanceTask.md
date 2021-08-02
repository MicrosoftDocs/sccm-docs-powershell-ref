---
description: Gets maintenance tasks in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSiteMaintenanceTask
---

# Get-CMSiteMaintenanceTask

## SYNOPSIS
Gets maintenance tasks in Configuration Manager.

## SYNTAX

```
Get-CMSiteMaintenanceTask [-Name <String>] [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSiteMaintenanceTask** cmdlet gets maintenance tasks in Configuration Manager.
A maintenance task is a task in Configuration Manager that performs maintenance on sites and databases.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a maintenance task

This example gets the maintenance task named **Backup SMS Site Server** for the Configuration Manager site that has the site code **CM1**.

```powershell
Get-CMSiteMaintenanceTask -SiteCode "CM1" -MaintenanceTaskName "Backup SMS Site Server"
```

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

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: ItemName, MaintenanceTaskName, TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_SCI_SQLTask
### IResultObject#SMS_SCI_SQLTask
## NOTES

## RELATED LINKS

[Set-CMSiteMaintenanceTask](Set-CMSiteMaintenanceTask.md)


