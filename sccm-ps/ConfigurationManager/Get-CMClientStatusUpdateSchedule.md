---
description: Gets a schedule interval of the client status update task.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMClientStatusUpdateSchedule
---

# Get-CMClientStatusUpdateSchedule

## SYNOPSIS
Gets a schedule interval of the client status update task.

## SYNTAX

```
Get-CMClientStatusUpdateSchedule [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientStatusUpdateSchedule** cmdlet gets a schedule interval of the client status update task.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Gets a client status update schedule
```
PS XYZ:\> Get-CMClientStatusUpdateSchedule
Interval Unit
-------- ----
       1 Days
```

This command gets a client status update schedule.

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

### ClientStatusUpdateSchedule
## NOTES

## RELATED LINKS

[Set-CMClientStatusUpdateSchedule](Set-CMClientStatusUpdateSchedule.md)

[Get-CMClientStatusSetting](Get-CMClientStatusSetting.md)

[Set-CMClientStatusSetting](Set-CMClientStatusSetting.md)


