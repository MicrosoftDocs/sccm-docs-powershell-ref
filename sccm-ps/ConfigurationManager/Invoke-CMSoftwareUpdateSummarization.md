---
description: Runs the Configuration Manager software update summarization.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Invoke-CMSoftwareUpdateSummarization
---

# Invoke-CMSoftwareUpdateSummarization

## SYNOPSIS
Runs the Configuration Manager software update summarization.

## SYNTAX

```
Invoke-CMSoftwareUpdateSummarization [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMSoftwareUpdateSummarization** cmdlet runs the software update summarization in Configuration Manager immediately.
Configuration Manager summarizes software update status on a regular schedule.
This cmdlet does not reset the time for the next automatic summarization.

You can use the Get-CMSoftwareUpdateSummarizationSchedule cmdlet to view the current schedule and the [Set-CMSoftwareUpdateSummarizationSchedule](Set-CMSoftwareUpdateSummarizationSchedule.md) cmdlet to change the schedule.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Run software update summarization
```
PS XYZ:\>Invoke-CMSoftwareUpdateSummarization
```

This command runs the software update summarization immediately, instead of waiting for the next scheduled time.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdateSummarizationSchedule](Get-CMSoftwareUpdateSummarizationSchedule.md)

[Set-CMSoftwareUpdateSummarizationSchedule](Set-CMSoftwareUpdateSummarizationSchedule.md)


