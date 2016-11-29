---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833678
schema: 2.0.0
ms.assetid: 8104F0AD-BD4E-43FB-9E4B-E347CEE0A70C
---

# Set-CMBaselineSummarizationSchedule

## SYNOPSIS
Configures the summarization schedule for configuration baseline data.

## SYNTAX

```
Set-CMBaselineSummarizationSchedule -Interval <Int32> [-Unit <SummarizationScheduleUnit>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMBaselineSummarizationSchedule** cmdlet configures the schedule by which the configuration baseline data in the Microsoft System Center Configuration Manager is updated with the latest information from the site database.

## EXAMPLES

### Example 1: Set the configuration baseline update schedule
```
PS C:\>Set-CMBaselineSummarizationSchedule -Interval 6 -Unit "Hours"
```

This command schedules Configuration Manager to automatically update the configuration baseline data every six hours.

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

### -Interval
Specifies an amount of time, as an integer.
This value works with the unit type you specify in the *Unit* parameter.
Valid values for this parameter depend on the unit that you select: 

- Minutes: 10 through 59. 
- Hours: 1 through 23. 
- Days: 1 through 31.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Unit
Specifies a unit to use to define an interval for the summarization schedule.
Valid values are: 

- Days
- Hours
- Minutes

```yaml
Type: SummarizationScheduleUnit
Parameter Sets: (All)
Aliases: 
Accepted values: Minutes, Hours, Days

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

[Get-CMBaselineSummarizationSchedule](./Get-CMBaselineSummarizationSchedule.md)

[Invoke-CMBaselineSummarization](./Invoke-CMBaselineSummarization.md)


