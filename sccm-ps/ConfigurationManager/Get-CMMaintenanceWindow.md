---
description: Get the maintenance windows for a collection.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 06/16/2021
schema: 2.0.0
title: Get-CMMaintenanceWindow
---

# Get-CMMaintenanceWindow

## SYNOPSIS

Get the maintenance windows for a collection.

## SYNTAX

### ByValue (Default)
```
Get-CMMaintenanceWindow [-InputObject] <IResultObject> [-MaintenanceWindowName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionId
```
Get-CMMaintenanceWindow [-CollectionId] <String> [-MaintenanceWindowName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionName
```
Get-CMMaintenanceWindow [-CollectionName] <String> [-MaintenanceWindowName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the maintenance windows for the specified collection. You can also filter the results to a specific maintenance window.

For more information on maintenance windows, see [How to use maintenance windows in Configuration Manager](/mem/configmgr/core/clients/manage/collections/use-maintenance-windows).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get enabled maintenance windows for a collection by ID

This command gets the maintenance windows that are enabled for the specified collection.

```powershell
Get-CMMaintenanceWindow -CollectionID "XYZ0004D" | Where-Object { $_.IsEnabled }
```

### Example 2: Get all maintenance windows for a collection object

This example first gets a collection object, and then passes that on the pipeline to get a maintenance window by its name.

```powershell
$coll = Get-CMCollection -CollectionID 'XYZ0003F'
$coll | Get-CMMaintenanceWindow -MaintenanceWindowName 'nightly SUM window'
```

### Example 3: Get the schedule for a maintenance window

This example first gets a maintenance window for a specific collection. It then converts the ServiceWindowSchedules property to display the maintenance window's schedule.

```powershell
$mw = Get-CMMaintenanceWindow -CollectionID "XYZ000AB"
Convert-CMSchedule -ScheduleString $mw.ServiceWindowSchedules
```

## PARAMETERS

### -CollectionId

Specify a collection ID to query for its maintenance windows. This ID is a standard collection ID, for example `XYZ0003F`.

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

Specify a collection name to query for its maintenance windows.

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

Specify a collection object to query for its maintenance windows. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

### -MaintenanceWindowName

Specify the name of a maintenance window on the targeted collection. By default, **Get-CMMaintenanceWindow** returns all maintenance windows. Use this parameter to filter the results to the specified window name.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_ServiceWindow
## NOTES

For more information on this return object and its properties, see [SMS_ServiceWindow server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_servicewindow-server-wmi-class).

## RELATED LINKS

[New-CMMaintenanceWindow](New-CMMaintenanceWindow.md)

[Remove-CMMaintenanceWindow](Remove-CMMaintenanceWindow.md)

[Set-CMMaintenanceWindow](Set-CMMaintenanceWindow.md)

[How to use maintenance windows in Configuration Manager](/mem/configmgr/core/clients/manage/collections/use-maintenance-windows)
