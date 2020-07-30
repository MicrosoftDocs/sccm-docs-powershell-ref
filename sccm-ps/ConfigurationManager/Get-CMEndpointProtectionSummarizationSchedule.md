---
description: Gets an Endpoint Protection summarization schedule.
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMEndpointProtectionSummarizationSchedule
---

# Get-CMEndpointProtectionSummarizationSchedule

## SYNOPSIS
Gets an Endpoint Protection summarization schedule.

## SYNTAX

```
Get-CMEndpointProtectionSummarizationSchedule [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEndpointProtectionSummarizationSchedule** cmdlet gets a System Center 2016 Endpoint Protection summarization schedule.
For more information about Endpoint Protection summarization schedules, see [How to Monitor Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508769(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get an Endpoint Protection summarization schedule
```
PS XYZ:\> Get-CMEndpointProtectionSummarizationSchedule
```

This command gets an Endpoint Protection summarization schedule.

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

### EndpointProtectionSummarizationSchedule

## NOTES

## RELATED LINKS

[Set-CMEndpointProtectionSummarizationSchedule](Set-CMEndpointProtectionSummarizationSchedule.md)


