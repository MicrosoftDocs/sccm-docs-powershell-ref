---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: 
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
PS C:\>Set-CMMaintenanceWindow -Name "DiskCleanup"-CollectionID "AAA0004D" -ApplyToTaskSequenceOnly
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


