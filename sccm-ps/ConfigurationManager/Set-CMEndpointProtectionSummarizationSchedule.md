---
author: aczechowski
description: Modifies an Endpoint Protection summarization schedule.
external help file: AdminUI.PS.Sum.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMEndpointProtectionSummarizationSchedule
titleSuffix: Configuration Manager
---

# Set-CMEndpointProtectionSummarizationSchedule

## SYNOPSIS
Modifies an Endpoint Protection summarization schedule.

## SYNTAX

```
Set-CMEndpointProtectionSummarizationSchedule -Interval <Int32> [-Unit <SummarizationScheduleUnit>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMEndpointProtectionSummarizationSchedule** cmdlet modifies the settings of an System Center 2016 Endpoint Protection summarization schedule.
For more information about Endpoint Protection summarization schedules, see [How to Monitor Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268428) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Modify an Endpoint Protection summarization schedules
```
PS XYZ:\> Set-CMEndpointProtectionSummarizationSchedule -Interval 10 -UnitType "Days"
```

This command modifies the interval and unit values to specify that 10 days pass before the Endpoint Protection Summarization Schedule runs again.

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

### -Unit
Specifies a unit to use to define an interval for the summarization schedule.
The acceptable values for this parameter are:

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMEndpointProtectionSummarizationSchedule](Get-CMEndpointProtectionSummarizationSchedule.md)


