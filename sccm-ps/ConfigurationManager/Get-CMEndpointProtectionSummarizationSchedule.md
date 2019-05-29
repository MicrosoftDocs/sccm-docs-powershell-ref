---
title: Get-CMEndpointProtectionSummarizationSchedule
titleSuffix: Configuration Manager
description: Gets an Endpoint Protection summarization schedule.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
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
For more information about Endpoint Protection summarization schedules, see [How to Monitor Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268428) on TechNet.

## EXAMPLES

### Example 1: Get an Endpoint Protection summarization schedule
```
PS C:\> Get-CMEndpointProtectionSummarizationSchedule
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMEndpointProtectionSummarizationSchedule](Set-CMEndpointProtectionSummarizationSchedule.md)


