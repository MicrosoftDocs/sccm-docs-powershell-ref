---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: 4BCE08DA-01DE-4CF2-86A8-F6CA8DD022E2
online version: https://go.microsoft.com/fwlink/?linkid=833749
schema: 2.0.0
---

# Set-CMCollectionPowerManagement

## SYNOPSIS
Configures power management settings for a device collection.

## SYNTAX

### ByValueApply (Default)
```
Set-CMCollectionPowerManagement -InputObject <IResultObject> [-Apply] [-PeakStartTime <DateTime>]
 [-PeakEndTime <DateTime>] [-WakeupTime <DateTime>] [-PeakPlan <PowerSchema>] [-NonPeakPlan <PowerSchema>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### ByNameApply
```
Set-CMCollectionPowerManagement -CollectionName <String> [-Apply] [-PeakStartTime <DateTime>]
 [-PeakEndTime <DateTime>] [-WakeupTime <DateTime>] [-PeakPlan <PowerSchema>] [-NonPeakPlan <PowerSchema>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### ByIdApply
```
Set-CMCollectionPowerManagement -CollectionId <String> [-Apply] [-PeakStartTime <DateTime>]
 [-PeakEndTime <DateTime>] [-WakeupTime <DateTime>] [-PeakPlan <PowerSchema>] [-NonPeakPlan <PowerSchema>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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

## EXAMPLES

### Example 1: Configure power management settings by using the pipeline
```
PS C:\> Get-CMCollection -Name "DeviceCol1" | Set-CMCollectionPowerManagement -NeverApply -PassThru
```

This command gets the device collection object named DeviceCol1 and uses the pipeline operator to pass the object to **Set-CMCollectionPowerManagement**.
**Set-CMCollectionPowerManagagement** configures deviceCol1 to never apply power management settings to the computers in that collection.

### Example 2: Configure power management settings by name
```
PS C:\> Set-CMCollectionPowerManagement -CollectionName "DeviceCol2" -Apply -PeakStartTime 8:00am -PeakEndTime 6:00pm -PeakPlan (Get-CMPowerManagementSchema -Peak -Name "Balanced (ConfigMgr)") -NonPeakPlan (Get-CMPowerManagementSchema -NonPeak -Name "Power Saver (ConfigMgr)") -WakeupTime 4:00am
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
Parameter Sets: ByIdNone, ByIdNever, ByIdApply
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
Parameter Sets: ByNameNone, ByNameNever, ByNameApply
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
Parameter Sets: ByNameNever, ByIdNever, ByValueNever
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

### -None
Indicates that no power management settings are set for the specified collection.

```yaml
Type: SwitchParameter
Parameter Sets: ByNameNone, ByIdNone, ByValueNone
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
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

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Get-CMPowerManagementSchema](Get-CMPowerManagementSchema.md)

[New-CMPowerManagementCustomPlan](New-CMPowerManagementCustomPlan.md)


