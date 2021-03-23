---
description: Creates a custom power management plan.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMPowerManagementCustomPlan
---

# New-CMPowerManagementCustomPlan

## SYNOPSIS
Creates a custom power management plan.

## SYNTAX

### Peak (Default)
```
New-CMPowerManagementCustomPlan [-AllowHybridSleepAC <Boolean>] [-AllowHybridSleepDC <Boolean>]
 [-AllowStandbyAC <Boolean>] [-AllowStandbyDC <Boolean>] [-CriticalBatteryAC <PowerSettingAction>]
 [-CriticalBatteryDC <PowerSettingAction>] [-Description <String>] [-DisplayOffMinAC <Int32>]
 [-DisplayOffMinDC <Int32>] [-HardDiskIdleMinAC <Int32>] [-HardDiskIdleMinDC <Int32>] [-HibernateMinAC <Int32>]
 [-HibernateMinDC <Int32>] [-LidDownAC <PowerSettingAction>] [-LidDownDC <PowerSettingAction>]
 [-LowBatteryAC <PowerSettingAction>] [-LowBatteryDC <PowerSettingAction>] [-Name <String>] [-NoAllowStandby]
 [-NoCriticalBattery] [-NoDisplayOff] [-NoHardDiskIdle] [-NoHibernate] [-NoHybridSleep] [-NoLidDown]
 [-NoLowBattery] [-NoPowerButton] [-NoRequirePasswordOnWake] [-NoSleep] [-NoSleepButton] [-NoSleepIdle]
 [-NoStartButton] [-NoWakeOnTimer] [-Peak] [-PowerButtonAC <PowerSettingAction>]
 [-PowerButtonDC <PowerSettingAction>] [-RequirePasswordOnWakeAC <Boolean>]
 [-RequirePasswordOnWakeDC <Boolean>] [-SleepButtonAC <PowerSettingAction>]
 [-SleepButtonDC <PowerSettingAction>] [-SleepIdlePctAC <Int32>] [-SleepIdlePctDC <Int32>]
 [-SleepMinAC <Int32>] [-SleepMinDC <Int32>] [-StartButtonAC <PowerSettingAction>]
 [-StartButtonDC <PowerSettingAction>] [-WakeOnTimerAC <Boolean>] [-WakeOnTimerDC <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### NonPeak
```
New-CMPowerManagementCustomPlan [-AllowHybridSleepAC <Boolean>] [-AllowHybridSleepDC <Boolean>]
 [-AllowStandbyAC <Boolean>] [-AllowStandbyDC <Boolean>] [-CriticalBatteryAC <PowerSettingAction>]
 [-CriticalBatteryDC <PowerSettingAction>] [-Description <String>] [-DisplayOffMinAC <Int32>]
 [-DisplayOffMinDC <Int32>] [-HardDiskIdleMinAC <Int32>] [-HardDiskIdleMinDC <Int32>] [-HibernateMinAC <Int32>]
 [-HibernateMinDC <Int32>] [-LidDownAC <PowerSettingAction>] [-LidDownDC <PowerSettingAction>]
 [-LowBatteryAC <PowerSettingAction>] [-LowBatteryDC <PowerSettingAction>] [-Name <String>] [-NoAllowStandby]
 [-NoCriticalBattery] [-NoDisplayOff] [-NoHardDiskIdle] [-NoHibernate] [-NoHybridSleep] [-NoLidDown]
 [-NoLowBattery] [-NonPeak] [-NoPowerButton] [-NoRequirePasswordOnWake] [-NoSleep] [-NoSleepButton]
 [-NoSleepIdle] [-NoStartButton] [-NoWakeOnTimer] [-PowerButtonAC <PowerSettingAction>]
 [-PowerButtonDC <PowerSettingAction>] [-RequirePasswordOnWakeAC <Boolean>]
 [-RequirePasswordOnWakeDC <Boolean>] [-SleepButtonAC <PowerSettingAction>]
 [-SleepButtonDC <PowerSettingAction>] [-SleepIdlePctAC <Int32>] [-SleepIdlePctDC <Int32>]
 [-SleepMinAC <Int32>] [-SleepMinDC <Int32>] [-StartButtonAC <PowerSettingAction>]
 [-StartButtonDC <PowerSettingAction>] [-WakeOnTimerAC <Boolean>] [-WakeOnTimerDC <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMPowerManagementCustomPlan** cmdlet creates a custom power management plan.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create parameters for a custom power management plan and store them in a variable
```
PS XYZ:\>$PlanParams = @{
    Name = "test"
    Description = "comments"
    DisplayOffMinAC = 20
    DisplayOffMinDC = 20
    SleepMinAC = 65
    SleepMinDC = 20
    RequirePasswordOnWakeAC = $true
    RequirePasswordOnWakeDC = $false
    PowerButtonAC = "None"
    PowerButtonDC = "Sleep"
    StartButtonAC = "Hibernate"
    StartButtonDC = "Sleep"
    SleepButtonAC= "None"
    SleepButtonDC = "Sleep"
    LidDownAC = "None"
    LidDownDC = "Sleep"
    HardDiskIdleMinAC = 25
    HardDiskIdleMinDC = 10
    HibernateMinAC = 10
    HibernateMinDC = 5
    LowBatteryAC = "None"
    LowBatteryDC = "Sleep"
    CriticalBatteryAC = "None"
    CriticalBatteryDC = "ShutDown"
    AllowHybridSleepAC = $false
    AllowHybridSleepDC = $true
    AllowStandbyAC= $false
    AllowStandbyDC = $true
    SleepIdlePctDC = 10
    SleepIdlePctAC = 15
    WakeOnTimerAC = $true
    WakeOnTimerDC = $false
}
```

This command creates an array of parameters and their settings for a custom power management plan, and then stores the array in the $PlanParams variable.
This variable can now be used to create a custom plan.

### Example 2: Create a custom peak power management plan to configure a device collection
```
PS XYZ:\> $PeakPlan = New-CMPowerManagementCustomPlan -Peak @planParams
PS XYZ:\> Set-CMCollectionPowerManagement -CollectionName "deviceCol1" -PeakPlan $PeakPlan
```

The first command uses the parameters set in Example 1 to create a custom peak power management plan object, which it then stores in the $PeakPlan variable.

The second command uses the custom plan stored in $PeakPlan to configure the power management settings for the device collection named deviceCol01.

### Example 3: Create a custom non-peak power management plan to configure a device collection
```
PS XYZ:\> $NonPeakPlan = New-CMPowerManagementCustomPlan -NonPeak @planParams
PS XYZ:\> Set-CMCollectionPowerManagement -CollectionName "deviceCol2" -NonPeakPlan $NonPeakPlan
```

The first command uses the parameters set in Example 1 to create a custom non-peak power management plan object, which it then stores in the $NonPeakPlan variable.

The second command uses the custom plan stored in $NonPeakPlan to configure the power management settings for the device collection named deviceCol02.

## PARAMETERS

### -AllowHybridSleepAC
Indicates whether Windows saves a hibernation file when entering sleep when the device is plugged in.
A hibernation file can be used to restore the computer's state in the event of power loss while it has entered sleep.

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

### -AllowHybridSleepDC
Indicates whether Windows saves a hibernation file when entering sleep when the device is running on battery power.
A hibernation file can be used to restore the computer's state in the event of power loss while it has entered sleep.

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

### -AllowStandbyAC
Indicates whether to allow the computer to be on standby when the device is plugged in.
This still consumes some power, but enables the computer to wake faster.

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

### -AllowStandbyDC
Indicates whether to allow the computer to be on standby when the device running on battery power.
This still consumes some power, but enables the computer to wake faster.

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

### -CriticalBatteryAC
Specifies the action to take when the computer's battery reaches the specified critical battery notification when the device is plugged in.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CriticalBatteryDC
Specifies the action to take when the computer's battery reaches the specified critical battery notification when the device is running on batter power.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the power management plan.

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

### -DisplayOffMinAC
Specifies the length of time, in minutes, that the computer must be inactive before the display is turned off when the device is plugged in.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayOffMinDC
Specifies the length of time, in minutes, that the computer must be inactive before the display is turned off when the device running on battery power.

```yaml
Type: Int32
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

### -HardDiskIdleMinAC
Specifies the length of time, in minutes, that the computer's hard disk must be inactive before it is turned off when the device is plugged in.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HardDiskIdleMinDC
Specifies the length of time, in minutes, that the computer's hard disk must be inactive before it is turned off when the device is running on battery power.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HibernateMinAC
Specifies the length of time, in minutes, that the computer must be inactive before it enters hibernate when the device is plugged in.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HibernateMinDC
Specifies the length of time, in minutes, that the computer must be inactive before it enters hibernate when the device is running on battery power.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LidDownAC
Specifies the action that occurs when the user closes the lid of a portable computer when the device is plugged in.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LidDownDC
Specifies the action that occurs when the user closes the lid of a portable computer when the device is running on battery power.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LowBatteryAC
Specifies the action that occurs when the computer's battery reaches the specified low battery notification level when the device is plugged in.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LowBatteryDC
Specifies the action that occurs when the computer's battery reaches the specified low battery notification level when the device is running on battery power.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the power management plan.

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

### -NoAllowStandby
Indicates that the "Allow standby state when sleeping action" property is not included in this power management plan.

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

### -NoCriticalBattery
Indicates that the "Critical battery action" property is not included in this power management plan.

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

### -NoDisplayOff
Indicates that the "Turn off display after (minutes)" property is not included in this power management plan.

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

### -NoHardDiskIdle
Indicates that the "Turn off hard disk after (minutes)" property is not included in this power management plan.

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

### -NoHibernate
Indicates that the "Hibernate after (minutes)" property is not included in this power management plan.

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

### -NoHybridSleep
Indicates that the "Allow hybrid sleep" property is not included in this power management plan.

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

### -NoLidDown
Indicates that the "Lid close action" property is not included in this power management plan.

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

### -NoLowBattery
Indicates that the "Low battery action" property is not included in this power management plan.

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

### -NonPeak
Indicates that this is a non-peak plan.

```yaml
Type: SwitchParameter
Parameter Sets: NonPeak
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoPowerButton
Indicates that the "Power button action" property is not included in this power management plan.

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

### -NoRequirePasswordOnWake
Indicates that the "Require a password on wakeup" property is not included in this power management plan.

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

### -NoSleep
Indicates that the "Sleep after (minutes)" property is not included in this power management plan.

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

### -NoSleepButton
Indicates that the "Sleep button action" property is not included in this power management plan.

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

### -NoSleepIdle
Indicates that the "Required idleness to sleep (%)" property is not included in this power management plan.

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

### -NoStartButton
Indicates that the "Start menu power button" property is not included in this power management plan.

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

### -NoWakeOnTimer
Indicates that the "Enable Windows wake up timer for desktop computers" property is not included in this power management plan.

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

### -Peak
Indicates that this is a peak plan.

```yaml
Type: SwitchParameter
Parameter Sets: Peak
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PowerButtonAC
Specifies the action that is taken when the computer's power button is pressed when the device is plugged in.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PowerButtonDC
Specifies the action that is taken when the computer's power button is pressed when the device is running on battery power.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequirePasswordOnWakeAC
Indicates whether a password is required to unlock the computer when it enters wake from sleep when the device is plugged in.

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

### -RequirePasswordOnWakeDC
Indicates whether a password is required to unlock the computer when it enters wake from sleep when the device is running on battery power.

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

### -SleepButtonAC
Specifies the action that occurs when you press the computer's Sleep button when the device is plugged in.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SleepButtonDC
Specifies the action that occurs when you press the computer's Sleep button when the device is running on battery power.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: None, Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SleepIdlePctAC
Specifies the percentage of idle time on the computer processor time required for the computer to enter sleep when the device is plugged in.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SleepIdlePctDC
Specifies the percentage of idle time on the computer processor time required for the computer to enter sleep when the device is running on battery power.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SleepMinAC
Specifies the length of time, in minutes, that the computer must be in active before it enters sleep when the device is plugged in.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SleepMinDC
Specifies the length of time, in minutes, that the computer must be in active before it enters sleep when the device is running on battery power.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartButtonAC
Specifies the action that occurs when you press the computer's Start menu power button when the device is plugged in.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartButtonDC
Specifies the action that occurs when you press the computer's Start menu power button when the device is running on battery power.
Valid values are:

- None
- Sleep
- Hibernate
- Shutdown

```yaml
Type: PowerSettingAction
Parameter Sets: (All)
Aliases:
Accepted values: Sleep, Hibernate, Shutdown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeOnTimerAC
Indicates whether the build-in Windows timer is enabled when the device is plugged in.
Power management can use the Windows timer to wake a desktop computer.
When a desktop computer is woken by using the Windows wake up timer, it will remain awake for 10 minutes by default to allow time for the computer to install any updates or to receive policy.

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

### -WakeOnTimerDC
Indicates whether the build-in Windows timer is enabled when the device is running on battery power.
Power management can use the Windows timer to wake a desktop computer.
When a desktop computer is woken by using the Windows wake up timer, it will remain awake for 10 minutes by default to allow time for the computer to install any updates or to receive policy.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.AdminConsole.CollectionProperty.PowerSchema

## NOTES

## RELATED LINKS

[Set-CMCollectionPowerManagement](Set-CMCollectionPowerManagement.md)


