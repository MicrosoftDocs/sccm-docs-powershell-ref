---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833915
schema: 2.0.0
ms.assetid: CACE0105-30EC-4667-9F58-0BB43A6391B4
---

# Set-CMMaintenanceWindow

## SYNOPSIS
Modifies a maintenance window.

## SYNTAX

### ByCollectionMWValue (Default)
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] -Collection <IResultObject>
 [-IsEnabled <Boolean>] [-Schedule <IResultObject>] -MaintenanceWindow <IResultObject>
 [-ApplyToTaskSequenceOnly] [-ApplyToSoftwareUpdateOnly] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] -Collection <IResultObject>
 [-IsEnabled <Boolean>] [-Schedule <IResultObject>] -MaintenanceWindowName <String> [-ApplyToTaskSequenceOnly]
 [-ApplyToSoftwareUpdateOnly] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByCollectionIdMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] -CollectionId <String> [-IsEnabled <Boolean>]
 [-Schedule <IResultObject>] -MaintenanceWindowName <String> [-ApplyToTaskSequenceOnly]
 [-ApplyToSoftwareUpdateOnly] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByCollectionIdMWValue
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] -CollectionId <String> [-IsEnabled <Boolean>]
 [-Schedule <IResultObject>] -MaintenanceWindow <IResultObject> [-ApplyToTaskSequenceOnly]
 [-ApplyToSoftwareUpdateOnly] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByCollectionNameMWValue
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] -CollectionName <String> [-IsEnabled <Boolean>]
 [-Schedule <IResultObject>] -MaintenanceWindow <IResultObject> [-ApplyToTaskSequenceOnly]
 [-ApplyToSoftwareUpdateOnly] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByCollectionNameMWName
```
Set-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] -CollectionName <String> [-IsEnabled <Boolean>]
 [-Schedule <IResultObject>] -MaintenanceWindowName <String> [-ApplyToTaskSequenceOnly]
 [-ApplyToSoftwareUpdateOnly] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMMaintenanceWindow** cmdlet modifies a maintenance window associated with a collection.
Maintenance windows are periods of time reserved for write operations such as applying software updates, installing software, or configuring computer settings.

## EXAMPLES

### Example 1: Modify a maintenance window
```
PS C:\> Set-CMMaintenanceWindow -Name "DiskCleanup"-CollectionID "AAA0004D" -ApplyToTaskSequenceOnly
```

This command modifies the maintenance window named DiskCleanup, a window associated with the collection AAA0004D.
In this example, the maintenance window is configured to apply only to task sequences.

## PARAMETERS

### -ApplyTo


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
Indicates that the maintenance window is used to apply software updates only.

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
Indicates that the maintenance window is used to apply task sequences only.

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

### -Collection
Specifies a Configuration Manager maintenance window object.
To obtain a maintenance window object, use the [Get-CMMaintenanceWindow](./Get-CMMaintenanceWindow.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByCollectionMWValue, ByCollectionMWName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of the collection that the maintenance window applies to.

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
Specifies the name of the maintenance window.

```yaml
Type: String
Parameter Sets: ByCollectionNameMWValue, ByCollectionNameMWName
Aliases: 
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

### -IsEnabled


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


```yaml
Type: IResultObject
Parameter Sets: ByCollectionMWValue, ByCollectionIdMWValue, ByCollectionNameMWValue
Aliases: ScheduleWindow
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaintenanceWindowName
Specifies the name of the maintenance window.

```yaml
Type: String
Parameter Sets: ByCollectionMWName, ByCollectionIdMWName, ByCollectionNameMWName
Aliases: Name
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
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

### -Schedule
Specifies a **CMSchedule** object.
The schedule specifies when the maintenance window occurs.
To create a **CMSchedule** object, use the [New-CMSchedule](./New-CMSchedule.md) cmdlet.

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

[Get-CMMaintenanceWindow](./Get-CMMaintenanceWindow.md)

[New-CMMaintenanceWindow](./New-CMMaintenanceWindow.md)

[New-CMSchedule](./New-CMSchedule.md)

[Remove-CMMaintenanceWindow](./Remove-CMMaintenanceWindow.md)
