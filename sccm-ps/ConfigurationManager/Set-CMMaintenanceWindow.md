---
description: Modify a maintenance window.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 06/16/2021
schema: 2.0.0
title: Set-CMMaintenanceWindow
---

# Set-CMMaintenanceWindow

## SYNOPSIS

Modify a maintenance window.

## SYNTAX

### ByValueMWValue (Default)
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -InputObject <IResultObject> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindow <IResultObject> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -CollectionId <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindowName <String> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdMWValue
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -CollectionId <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindow <IResultObject> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -CollectionName <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindowName <String> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameMWValue
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -CollectionName <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindow <IResultObject> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] -InputObject <IResultObject> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -MaintenanceWindowName <String> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure a maintenance window on a collection.

For more information on maintenance windows, see [How to use maintenance windows in Configuration Manager](/mem/configmgr/core/clients/manage/collections/use-maintenance-windows).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a maintenance window to only apply to task sequence deployments

This command modifies the maintenance window named **DiskCleanup** on the collection with ID **XYZ0004D**.
It changes the maintenance window to apply only to task sequences.

```powershell
Set-CMMaintenanceWindow -Name "DiskCleanup" -CollectionID "XYZ0004D" -ApplyTo TaskSequencesOnly
```

## PARAMETERS

### -ApplyTo

Specify the type of maintenance window:

- `Any`: The maintenance window applies to all deployments.
- `SoftwareUpdatesOnly`: The maintenance window only applies to software update deployments.
- `TaskSequencesOnly`: The maintenance window only applies to task sequence deployments.

```yaml
Type: MaintenanceWindowApplyTo
Parameter Sets: (All)
Aliases:
Accepted values: Any, SoftwareUpdatesOnly, TaskSequencesOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToSoftwareUpdateOnly

This parameter is deprecated. Use the **ApplyTo** parameter with the **SoftwareUpdatesOnly** value.

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

### -ApplyToTaskSequenceOnly

This parameter is deprecated. Use the **ApplyTo** parameter with the **TaskSequencesOnly** value.

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

### -CollectionId

Specify the ID of a collection to configure a maintenance window. This ID is a standard collection ID, for example `XYZ0003F`.

```yaml
Type: String
Parameter Sets: ByCollectionIdMWName, ByCollectionIdMWValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of a collection to configure a maintenance window.

```yaml
Type: String
Parameter Sets: ByCollectionNameMWName, ByCollectionNameMWValue
Aliases:

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

### -InputObject

Specify an object for a collection to configure a maintenance window. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValueMWValue, ByValueMWName
Aliases: Collection, Site

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsEnabled

Use this parameter to configure if the maintenance window is active for the collection:

- `$true`: Enable the maintenance window. Deployments only run during the window's schedule.
- `$false`: Disable the maintenance window. Deployments run at any time as configured.

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

### -IsUtc

To configure the maintenance window schedule to use Coordinated Universal Time (UTC), set this parameter to `$true`.

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

### -MaintenanceWindow

Specify an maintenance window object to configure. To get this object, use the [Get-CMMaintenanceWindow](Get-CMMaintenanceWindow.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValueMWValue, ByCollectionIdMWValue, ByCollectionNameMWValue
Aliases: ScheduleWindow

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaintenanceWindowName

Specify the name of the maintenance window to configure.

```yaml
Type: String
Parameter Sets: ByCollectionIdMWName, ByCollectionNameMWName, ByValueMWName
Aliases: Name

Required: True
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

### -Schedule

Specify a schedule object for when the maintenance window occurs. To get this object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

The maintenance window object stores the schedule as a token string. To copy a schedule from another object, use the [Convert-CMSchedule](Convert-CMSchedule.md) cmdlet. For example, `Convert-CMSchedule -ScheduleString $mw1.ServiceWindowSchedules`.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Add this parameter to prompt for confirmation before running the cmdlet.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMMaintenanceWindow](Get-CMMaintenanceWindow.md)

[New-CMMaintenanceWindow](New-CMMaintenanceWindow.md)

[Remove-CMMaintenanceWindow](Remove-CMMaintenanceWindow.md)

[Convert-CMSchedule](Convert-CMSchedule.md)
[New-CMSchedule](New-CMSchedule.md)

[How to use maintenance windows in Configuration Manager](/mem/configmgr/core/clients/manage/collections/use-maintenance-windows)
