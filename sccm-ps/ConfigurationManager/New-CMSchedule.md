---
description: Create a Configuration Manager schedule token.
external help file: AdminUI.PS.Common.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/24/2020
schema: 2.0.0
title: New-CMSchedule
---

# New-CMSchedule

## SYNOPSIS

Create a Configuration Manager schedule token.

## SYNTAX

### RecurrenceNone (Default)
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] [-Nonrecurring] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurrenceNoneWithEnd
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] -End <DateTime> [-IsUtc] [-Nonrecurring]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurrenceWeeklyWithEnd
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] -End <DateTime> [-IsUtc] [-RecurCount <Int32>]
 -DayOfWeek <DayOfWeek> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RecurrenceMonthlyByDateWithEnd
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] -End <DateTime> [-IsUtc] [-RecurCount <Int32>]
 -DayOfMonth <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RecurMonthlyLastDayOfMonthWithEnd
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] -End <DateTime> [-IsUtc] [-RecurCount <Int32>]
 [-LastDayOfMonth] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RecurMonthlyByWeekdayWithEnd
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] -End <DateTime> [-IsUtc] [-RecurCount <Int32>]
 -DayOfWeek <DayOfWeek> -WeekOrder <ScheduleWeekOrder> [-OffsetDay <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurrenceIntervalWithEnd
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] -End <DateTime> [-IsUtc] -RecurCount <Int32>
 -RecurInterval <ScheduleInterval> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RecurrenceNoneWithDuration
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] -DurationInterval <ScheduleInterval>
 -DurationCount <Int32> [-Nonrecurring] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### RecurrenceWeeklyWithDuration
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] -DurationInterval <ScheduleInterval>
 -DurationCount <Int32> [-RecurCount <Int32>] -DayOfWeek <DayOfWeek> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurrenceMonthlyByDateWithDuration
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] -DurationInterval <ScheduleInterval>
 -DurationCount <Int32> [-RecurCount <Int32>] -DayOfMonth <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurMonthlyLastDayOfMonthWithDuration
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] -DurationInterval <ScheduleInterval>
 -DurationCount <Int32> [-RecurCount <Int32>] [-LastDayOfMonth] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurMonthlyByWeekdayWithDuration
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] -DurationInterval <ScheduleInterval>
 -DurationCount <Int32> [-RecurCount <Int32>] -DayOfWeek <DayOfWeek> -WeekOrder <ScheduleWeekOrder>
 [-OffsetDay <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RecurrenceIntervalWithDuration
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] -DurationInterval <ScheduleInterval>
 -DurationCount <Int32> -RecurCount <Int32> -RecurInterval <ScheduleInterval> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurrenceWeekly
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] [-RecurCount <Int32>] -DayOfWeek <DayOfWeek>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurrenceMonthlyByDate
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] [-RecurCount <Int32>] -DayOfMonth <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurMonthlyLastDayOfMonth
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] [-RecurCount <Int32>] [-LastDayOfMonth]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurMonthlyByWeekday
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] [-RecurCount <Int32>] -DayOfWeek <DayOfWeek>
 -WeekOrder <ScheduleWeekOrder> [-OffsetDay <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecurrenceInterval
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] -RecurCount <Int32>
 -RecurInterval <ScheduleInterval> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMSchedule** cmdlet creates a schedule token in Configuration Manager. Create schedule tokens to schedule events with differing frequencies such as daily, weekly, and monthly.

To decode and encode schedule tokens into and from an interval string, use the [Convert-CMSchedule](Convert-CMSchedule.md) cmdlet. You can then use the interval strings to set schedule properties when you define or modify Configuration Manager objects.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a schedule token

This command creates a schedule token that specifies that the event occurs on the last day of the month at the specified date and time (Wednesday, August 5, 2020 17:46:03 Pacific Daylight Time).

```PowerShell
$schedToken1 = New-CMSchedule -DayOfMonth 0 -Start "2020-08-05T17:46:03.7236084-07:00"
```

### Example 2: Create an offset schedule

The following example creates the following schedule:

- Starts on the current date
- On the second Monday of the month
- Recurs once

```PowerShell
$schedToken2 = New-CMSchedule -Start (Get-Date) -DayOfWeek Monday -WeekOrder Second -RecurCount 1 -OffsetDay 0
```

### Example 3: Create a schedule to run daily

This example creates a simple schedule that occurs daily forever. You can use this type of schedule when you deploy a configuration baseline.

```powershell
New-CMSchedule -DurationInterval Days -DurationCount 0 -RecurInterval Days -RecurCount 1
```

## PARAMETERS

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

### -DayOfMonth

Specifies the day of the month when the event occurs. Valid values range from 0 through 31. The default value is `0`, which indicates the last day of the month.

```yaml
Type: Int32
Parameter Sets: RecurrenceMonthlyByDateWithEnd, RecurrenceMonthlyByDateWithDuration, RecurrenceMonthlyByDate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DayOfWeek

Specifies the day of the week when the event occurs.

```yaml
Type: DayOfWeek
Parameter Sets: RecurrenceWeeklyWithEnd, RecurMonthlyByWeekdayWithEnd, RecurrenceWeeklyWithDuration, RecurMonthlyByWeekdayWithDuration, RecurrenceWeekly, RecurMonthlyByWeekday
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

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

### -DurationCount

Specifies the number of days during which the scheduled event occurs. Valid values range from 0 through 31. The default value is `0`, which indicates that the scheduled action continues indefinitely.

```yaml
Type: Int32
Parameter Sets: RecurrenceNoneWithDuration, RecurrenceWeeklyWithDuration, RecurrenceMonthlyByDateWithDuration, RecurMonthlyLastDayOfMonthWithDuration, RecurMonthlyByWeekdayWithDuration, RecurrenceIntervalWithDuration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DurationInterval

Specifies the time when the event occurs.

```yaml
Type: ScheduleInterval
Parameter Sets: RecurrenceNoneWithDuration, RecurrenceWeeklyWithDuration, RecurrenceMonthlyByDateWithDuration, RecurMonthlyLastDayOfMonthWithDuration, RecurMonthlyByWeekdayWithDuration, RecurrenceIntervalWithDuration
Aliases:
Accepted values: Minutes, Hours, Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -End

Specifies the date and time when the scheduled event ends.

```yaml
Type: DateTime
Parameter Sets: RecurrenceNoneWithEnd, RecurrenceWeeklyWithEnd, RecurrenceMonthlyByDateWithEnd, RecurMonthlyLastDayOfMonthWithEnd, RecurMonthlyByWeekdayWithEnd, RecurrenceIntervalWithEnd
Aliases:

Required: True
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

### -IsUtc

Indicates that the time is Coordinated Universal Time (UTC).

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

### -LastDayOfMonth

Indicates that the event occurs monthly on the last day of the month.

```yaml
Type: SwitchParameter
Parameter Sets: RecurMonthlyLastDayOfMonthWithEnd, RecurMonthlyLastDayOfMonthWithDuration, RecurMonthlyLastDayOfMonth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nonrecurring

Indicates that the scheduled event doesn't recur.

```yaml
Type: SwitchParameter
Parameter Sets: RecurrenceNone, RecurrenceNoneWithEnd, RecurrenceNoneWithDuration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OffsetDay

Starting in version 1906, use this parameter to configure an offset such as monthly by weekday.

```yaml
Type: Int32
Parameter Sets: RecurMonthlyByWeekdayWithEnd, RecurMonthlyByWeekdayWithDuration, RecurMonthlyByWeekday
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurCount

Specifies the number of recurrences of the scheduled event.

```yaml
Type: Int32
Parameter Sets: RecurrenceWeeklyWithEnd, RecurrenceMonthlyByDateWithEnd, RecurMonthlyLastDayOfMonthWithEnd, RecurMonthlyByWeekdayWithEnd, RecurrenceWeeklyWithDuration, RecurrenceMonthlyByDateWithDuration, RecurMonthlyLastDayOfMonthWithDuration, RecurMonthlyByWeekdayWithDuration, RecurrenceWeekly, RecurrenceMonthlyByDate, RecurMonthlyLastDayOfMonth, RecurMonthlyByWeekday
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Int32
Parameter Sets: RecurrenceIntervalWithEnd, RecurrenceIntervalWithDuration, RecurrenceInterval
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurInterval

Specifies the time when the scheduled event recurs.

```yaml
Type: ScheduleInterval
Parameter Sets: RecurrenceIntervalWithEnd, RecurrenceIntervalWithDuration, RecurrenceInterval
Aliases:
Accepted values: Minutes, Hours, Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScheduleString

Indicates that the schedule token is converted to an interval string.

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

### -Start

Specifies the date and time when the scheduled event occurs.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WeekOrder

Specifies the week of the month when the event occurs. The default value is `Last` (0).

```yaml
Type: ScheduleWeekOrder
Parameter Sets: RecurMonthlyByWeekdayWithEnd, RecurMonthlyByWeekdayWithDuration, RecurMonthlyByWeekday
Aliases:
Accepted values: Last, First, Second, Third, Fourth

Required: True
Position: Named
Default value: None
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

### None

## OUTPUTS

### IResultObject#SMS_ScheduleToken

For more information on this return object and its properties, see [SMS_ScheduleToken server WMI class](https://docs.microsoft.com/mem/configmgr/develop/reference/core/servers/configure/sms_scheduletoken-server-wmi-class).

### System.String

## NOTES

## RELATED LINKS

[Convert-CMSchedule](Convert-CMSchedule.md)
