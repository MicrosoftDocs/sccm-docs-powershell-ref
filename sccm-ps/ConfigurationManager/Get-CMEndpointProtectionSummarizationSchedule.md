---
description: Gets an Endpoint Protection summarization schedule.
external help file: AdminUI.PS.dll-Help.xml
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
For more information about Endpoint Protection summarization schedules, see [How to Monitor Endpoint Protection in Configuration Manager](/mem/configmgr/protect/deploy-use/monitor-endpoint-protection).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an Endpoint Protection summarization schedule
```
PS XYZ:\> Get-CMEndpointProtectionSummarizationSchedule
```

This command gets an Endpoint Protection summarization schedule.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### EndpointProtectionSummarizationSchedule
## NOTES

## RELATED LINKS

[Set-CMEndpointProtectionSummarizationSchedule](Set-CMEndpointProtectionSummarizationSchedule.md)


