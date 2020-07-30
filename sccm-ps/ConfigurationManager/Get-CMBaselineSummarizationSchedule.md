---
description: Gets the summarization schedule for configuration baseline data.
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMBaselineSummarizationSchedule
---

# Get-CMBaselineSummarizationSchedule

## SYNOPSIS
Gets the summarization schedule for configuration baseline data.

## SYNTAX

```
Get-CMBaselineSummarizationSchedule [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBaselineSummarizationSchedule** cmdlet gets the schedule by which the configuration baseline data in the Configuration Manager is updated with the latest information from the site database.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get the update schedule for configuration baseline data
```
PS XYZ:\> Get-CMBaselineSummarizationSchedule
```

This command gets the update schedule for configuration baseline data.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### BaselineSummarizationSchedule

## NOTES

## RELATED LINKS

[Set-CMBaselineSummarizationSchedule](Set-CMBaselineSummarizationSchedule.md)

[Invoke-CMBaselineSummarization](Invoke-CMBaselineSummarization.md)


