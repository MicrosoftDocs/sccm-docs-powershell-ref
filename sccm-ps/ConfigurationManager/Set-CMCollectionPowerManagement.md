---
description: Configures power management settings for a device collection.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMCollectionPowerManagement
---

# Set-CMCollectionPowerManagement

## SYNOPSIS
Configures power management settings for a device collection.

## SYNTAX

### ByValueApply (Default)
```
Set-CMCollectionPowerManagement [-Apply] -InputObject <IResultObject> [-NonPeakPlan <PowerSchema>] [-PassThru]
 [-PeakEndTime <DateTime>] [-PeakPlan <PowerSchema>] [-PeakStartTime <DateTime>] [-WakeupTime <DateTime>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameApply
```
Set-CMCollectionPowerManagement [-Apply] -CollectionName <String> [-NonPeakPlan <PowerSchema>] [-PassThru]
 [-PeakEndTime <DateTime>] [-PeakPlan <PowerSchema>] [-PeakStartTime <DateTime>] [-WakeupTime <DateTime>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdApply
```
Set-CMCollectionPowerManagement [-Apply] -CollectionId <String> [-NonPeakPlan <PowerSchema>] [-PassThru]
 [-PeakEndTime <DateTime>] [-PeakPlan <PowerSchema>] [-PeakStartTime <DateTime>] [-WakeupTime <DateTime>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdNone
```
Set-CMCollectionPowerManagement -CollectionId <String> [-None] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdNever
```
Set-CMCollectionPowerManagement -CollectionId <String> [-NeverApply] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameNone
```
Set-CMCollectionPowerManagement -CollectionName <String> [-None] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameNever
```
Set-CMCollectionPowerManagement -CollectionName <String> [-NeverApply] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueNone
```
Set-CMCollectionPowerManagement -InputObject <IResultObject> [-None] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueNever
```
Set-CMCollectionPowerManagement -InputObject <IResultObject> [-NeverApply] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCollectionPowerManagement** cmdlet configures power management settings for a device collection.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Configure power management settings by using the pipeline
```
PS XYZ:\> Get-CMCollection -Name "DeviceCol1" | Set-CMCollectionPowerManagement -NeverApply -PassThru
```

This command gets the device collection object named DeviceCol1 and uses the pipeline operator to pass the object to **Set-CMCollectionPowerManagement**.
**Set-CMCollectionPowerManagagement** configures deviceCol1 to never apply power management settings to the computers in that collection.

### Example 2: Configure power management settings by name
```
PS XYZ:\> Set-CMCollectionPowerManagement -CollectionName "DeviceCol2" -Apply -PeakStartTime 8:00am -PeakEndTime 6:00pm -PeakPlan (Get-CMPowerManagementSchema -Peak -Name "Balanced (ConfigMgr)") -NonPeakPlan (Get-CMPowerManagementSchema -NonPeak -Name "Power Saver (ConfigMgr)") -WakeupTime 4:00am
```

This command specifies power management settings for the device collection DeviceCol2.
During the peak hours of 8:00 AM to 6:00 PM, the peak power management plan named Balanced (ConfigMgr) is in effect.
During non-peak hours, the non-peak power management plan named Power Saver (ConfigMgr) is in effect.
The Windows timer is set to wake desktop computers install scheduled updates or software installations at 4:00 AM.

## PARAMETERS

### -Apply
Indicates that power management settings can be set for a specified device collection.

```yaml
Type: SwitchParameter
Parameter Sets: ByValueApply, ByNameApply, ByIdApply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
Specifies the collection ID of the device collection.

```yaml
Type: String
Parameter Sets: ByIdApply, ByIdNone, ByIdNever
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of the device collection.

```yaml
Type: String
Parameter Sets: ByNameApply, ByNameNone, ByNameNever
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
Specifies a device collection object.
To obtain a device collection object, use the Get-CMCollection or the Get-CMDeviceCollection cmdlets.

```yaml
Type: IResultObject
Parameter Sets: ByValueApply, ByValueNone, ByValueNever
Aliases: Collection, CollectionSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NeverApply
Indicates that power management settings will never be applied to computers in the specified collection.

```yaml
Type: SwitchParameter
Parameter Sets: ByIdNever, ByNameNever, ByValueNever
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -None
Indicates that no power management settings are set for the specified collection.

```yaml
Type: SwitchParameter
Parameter Sets: ByIdNone, ByNameNone, ByValueNone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonPeakPlan
Specifies a power management plan object for non-peak or non-business hours.
To obtain a power plan object , use the Get-CMPowerManagementSchema cmdlet.
To create a customized power plan, use New-CMPowerManagementCustomPlan cmdlet.

```yaml
Type: PowerSchema
Parameter Sets: ByValueApply, ByNameApply, ByIdApply
Aliases:

Required: False
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

### -PeakEndTime
Specifies the end time for peak hours.

```yaml
Type: DateTime
Parameter Sets: ByValueApply, ByNameApply, ByIdApply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeakPlan
Specifies a power management plan object for peak or business hours.
To obtain a power plan object, use Get-CMPowerManagementSchema cmdlet.
To create a customized power plan, use New-CMPowerManagementCustomPlan cmdlet.

```yaml
Type: PowerSchema
Parameter Sets: ByValueApply, ByNameApply, ByIdApply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PeakStartTime
Specifies the start time for peak hours.

```yaml
Type: DateTime
Parameter Sets: ByValueApply, ByNameApply, ByIdApply
Aliases: PeakStartHour

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeupTime
Specifies a time when the Windows timer wakes a desktop computer from sleep or hibernate to install scheduled updates or software installations.

```yaml
Type: DateTime
Parameter Sets: ByValueApply, ByNameApply, ByIdApply
Aliases:

Required: False
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

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Get-CMPowerManagementSchema](Get-CMPowerManagementSchema.md)

[New-CMPowerManagementCustomPlan](New-CMPowerManagementCustomPlan.md)


