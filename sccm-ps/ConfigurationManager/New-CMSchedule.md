---
author: aczechowski
description: Creates a Configuration Manager schedule token.
external help file: AdminUI.PS.Common.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMSchedule
titleSuffix: Configuration Manager
---

# New-CMSchedule

## SYNOPSIS
Creates a Configuration Manager schedule token.

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
 -DayOfWeek <DayOfWeek> -WeekOrder <ScheduleWeekOrder> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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
 -WeekOrder <ScheduleWeekOrder> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RecurrenceInterval
```
New-CMSchedule [-ScheduleString] [-Start <DateTime>] [-IsUtc] -RecurCount <Int32>
 -RecurInterval <ScheduleInterval> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSchedule** cmdlet creates a schedule token in Microsoft System Center Configuration Manager.

In Microsoft System Center Configuration Manager, you use schedule tokens to configure scheduling information.
You can create schedule tokens to schedule events with differing frequencies such as daily, weekly, and monthly.

Use the Convert-CMSchedule cmdlet to decode and encode schedule tokens into and from an interval string.
You can then use the interval strings to set schedule properties when you define or modify System Center Configuration Manager objects.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a schedule token
```
PS XYZ:\> New-CMSchedule -DayOfMonth 0 -DateTime "20120105185728.303000+000"
```

This command creates a schedule token that specifies that the event occurs on the last day of the month at the specified date and time.

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
Specifies the day of the month when the event occurs.
Valid values range from 0 through 31.
The default value is 0, which indicates the last day of the month.

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
The acceptable values for this parameter are:

- Sunday (default)
- Monday
- Tuesday
- Wednesday
- Thursday
- Friday
- Saturday

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

### -DurationCount
Specifies the number of days during which the scheduled event occurs.
Valid values range from 0 through 31.
The default value is 0, which indicates that the scheduled action continues indefinitely.

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
Indicates that the scheduled event does not recur.

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
Specifies the week of the month when the event occurs.
The acceptable values for this parameter are:

- 0: Last (default)
- 1: First
- 2: Second
- 3: Third
- 4: Fourth

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Convert-CMSchedule](Convert-CMSchedule.md)


