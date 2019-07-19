<<<<<<< HEAD
---
title: Set-CMSoftwareUpdateSummarizationSchedule
titleSuffix: Configuration Manager
description: Sets how often Configuration Manager summarizes the status of updates.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: 3A9B5B87-2CE5-432B-BB63-D4CA96E35350
online version: https://go.microsoft.com/fwlink/?linkid=834100
schema: 2.0.0
>>>>>>> master
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
You can use the [Invoke-CMSoftwareUpdateSummarization](Invoke-CMSoftwareUpdateSummarization.md) cmdlet to run the summarization immediately.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Schedule summarization interval and unit
```
PS XYZ:\> Set-CMSoftwareUpdateSummarizationSchedule -Interval 5 -Unit Days
```

This command sets the update summarization schedule to run every five days.

### Example 2: Change schedule interval
```
PS XYZ:\> Set-CMSoftwareUpdateSummarizationSchedule -Interval 7
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

[Get-CMSoftwareUpdateSummarizationSchedule](Get-CMSoftwareUpdateSummarizationSchedule.md)

[Invoke-CMSoftwareUpdateSummarization](Invoke-CMSoftwareUpdateSummarization.md)
