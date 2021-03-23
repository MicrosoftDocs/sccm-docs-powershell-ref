---
description: Displays the Configuration Manager schedule for software update summarization.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSoftwareUpdateSummarizationSchedule
---

# Get-CMSoftwareUpdateSummarizationSchedule

## SYNOPSIS
Displays the Configuration Manager schedule for software update summarization.

## SYNTAX

```
Get-CMSoftwareUpdateSummarizationSchedule [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateSummarizationSchedule** cmdlet displays the current schedule for software update summarization for Configuration Manager.
You can use the [Set-CMSoftwareUpdateSummarizationSchedule](Set-CMSoftwareUpdateSummarizationSchedule.md) cmdlet to change the schedule.
You can use the [Invoke-CMSoftwareUpdateSummarization](Invoke-CMSoftwareUpdateSummarization.md) cmdlet to run the summarization immediately.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Display the summarization schedule
```
PS XYZ:\> Get-CMSoftwareUpdateSummarizationSchedule
                               Interval                                    Unit
                               --------                                    ----
                                     12                                   Hours
```

This command displays the summarization schedule for software updates.
In this case, the schedule is every 12 hours.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### SoftwareUpdateSummarizationSchedule

## NOTES

## RELATED LINKS

[Set-CMSoftwareUpdateSummarizationSchedule](Set-CMSoftwareUpdateSummarizationSchedule.md)

[Invoke-CMSoftwareUpdateSummarization](Invoke-CMSoftwareUpdateSummarization.md)
