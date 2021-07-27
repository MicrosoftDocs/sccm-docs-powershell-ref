---
description: Create a maintenance window for a collection.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 06/16/2021
schema: 2.0.0
title: New-CMMaintenanceWindow
---

# New-CMMaintenanceWindow

## SYNOPSIS

Create a maintenance window for a collection.

## SYNTAX

### ByValue (Default)
```
New-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] [-InputObject] <IResultObject> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -Name <String> -Schedule <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByCollectionId
```
New-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] [-CollectionId] <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>] -Name <String>
 -Schedule <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByCollectionName
```
New-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] [-CollectionName] <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>] -Name <String>
 -Schedule <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a maintenance window for a collection.
Maintenance windows are recurring periods of time when the Configuration Manager client can run tasks. For example, apply software updates or install software.
This window makes sure that significant system changes only happen at times that don't affect productivity and uptime.

For more information on maintenance windows, see [How to use maintenance windows in Configuration Manager](/mem/configmgr/core/clients/manage/collections/use-maintenance-windows).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a maintenance window

The first command uses the **New-CMSchedule** cmdlet to create a schedule object, and then stores it in the `$MWSchedule` variable.

The second command creates a maintenance window named **MonthlySchedule** for the specified collection.
The maintenance window uses the schedule stored in the `$MWSchedule` variable.

```powershell
$MWSchedule = New-CMSchedule -DayOfWeek Friday -DurationCount 1 -DurationInterval Hours -RecurCount 1 -Start "10/12/2013 21:00:00"
New-CMMaintenanceWindow -CollectionId "XYZ0005D" -Name "MonthlySchedule" -Schedule $MWSchedule
```

### Example 2: Copy a maintenance window between collections

The first command gets a maintenance window from the collection with ID **XYZ0003F**. It then creates a maintenance window on the collection with ID **XYZ0005D** with the same name, same schedule, and only for software updates.

```powershell
$mw1 = Get-CMMaintenanceWindow -CollectionId "XYZ0003F" -MaintenanceWindowName "nightly SUM window"
New-CMMaintenanceWindow -CollectionId "XYZ0005D" -Name $mw1.Name -Schedule (Convert-CMSchedule -ScheduleString $mw1.ServiceWindowSchedules) -ApplyTo SoftwareUpdatesOnly
```

## PARAMETERS

### -ApplyTo

Specify the type of maintenance window to create:

- `Any`: The maintenance window applies to all deployments.
- `SoftwareUpdatesOnly`: The maintenance window only applies to software update deployments.
- `TaskSequencesOnly`: The maintenance window only applies to task sequence deployments.

If you don't specify this parameter, `Any` is the default.

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

Specify the ID of a collection to add the maintenance window. This ID is a standard collection ID, for example `XYZ0003F`.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of a collection to add the maintenance window.

```yaml
Type: String
Parameter Sets: ByCollectionName
Aliases:

Required: True
Position: 0
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

Specify an object for a collection to add the maintenance window. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection, Site

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsEnabled

To create a maintenance window on a collection, but not have it active, set this parameter to `$false`. If you don't include this parameter, this cmdlet enables the maintenance window.

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

To configure the maintenance window schedule to use Coordinated Universal Time (UTC), set this parameter to `$true`. If you don't include this parameter, the schedule uses local time.

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

### -Name

Specify the name of the maintenance window.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MaintenanceWindowName

Required: True
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

Required: True
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

### IResultObject#SMS_ServiceWindow
## NOTES

For more information on this return object and its properties, see [SMS_ServiceWindow server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_servicewindow-server-wmi-class).

## RELATED LINKS

[Get-CMMaintenanceWindow](Get-CMMaintenanceWindow.md)

[Remove-CMMaintenanceWindow](Remove-CMMaintenanceWindow.md)

[Set-CMMaintenanceWindow](Set-CMMaintenanceWindow.md)

[Convert-CMSchedule](Convert-CMSchedule.md)
[New-CMSchedule](New-CMSchedule.md)

[How to use maintenance windows in Configuration Manager](/mem/configmgr/core/clients/manage/collections/use-maintenance-windows)
