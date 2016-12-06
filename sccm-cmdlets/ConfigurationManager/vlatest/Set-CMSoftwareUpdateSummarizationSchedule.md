---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834100
schema: 2.0.0
ms.assetid: 3A9B5B87-2CE5-432B-BB63-D4CA96E35350
---

# Set-CMSoftwareUpdateSummarizationSchedule

## SYNOPSIS
Sets how often Configuration Manager summarizes the status of updates.

## SYNTAX

```
Set-CMSoftwareUpdateSummarizationSchedule -Interval <Int32> -Unit <SummarizationScheduleUnit> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdateSummarizationSchedule** cmdlet sets how often Microsoft System Center Configuration Manager summarizes the status of software updates for all the System Center Configuration Manager sites.
You can set the summary to run on an interval defined in days, hours, or minutes.
You can use the Invoke-CMSoftwareUpdateSummarization cmdlet to run the summarization immediately.

## EXAMPLES

### Example 1: Schedule summarization interval and unit
```
PS C:\>Set-CMSoftwareUpdateSummarizationSchedule -Interval 5 -Unit Days
```

This command sets the update summarization schedule to run every five days.

### Example 2: Change schedule interval
```
PS C:\>Set-CMSoftwareUpdateSummarizationSchedule -Interval 7
```

This command changes the interval for the update summarization schedule to seven.
The command does not change the unit.

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
This value works with the unit type you specify in the Unit parameter.
Valid values for this parameter depend on the unit that you select: 

-- Minutes: 10 through 59.
-- Hours: 1 through 23.
-- Days: 1 through 31.

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

### -PassThru


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

### -Unit
Specifies a unit to use to define an interval for the summarization schedule.
Valid values are: 

-- Days
-- Hours
-- Minutes

```yaml
Type: SummarizationScheduleUnit
Parameter Sets: (All)
Aliases: 
Accepted values: Days, Hours, Minutes
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdateSummarizationSchedule](./Get-CMSoftwareUpdateSummarizationSchedule.md)

[Invoke-CMSoftwareUpdateSummarization](./Invoke-CMSoftwareUpdateSummarization.md)


