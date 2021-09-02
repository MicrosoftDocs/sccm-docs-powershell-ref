---
description: Modifies the schedule interval of the client status update task.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMClientStatusUpdateSchedule
---

# Set-CMClientStatusUpdateSchedule

## SYNOPSIS
Modifies the schedule interval of the client status update task.

## SYNTAX

```
Set-CMClientStatusUpdateSchedule -Interval <Int32> -UnitType <ClientStatusUpdateScheduleUnit>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMClientStatusUpdateSchedule** cmdlet modifies the schedule interval of the client status update task.
For more information, see [How to Configure Client Status in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-client-status).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a client's status update schedule
```
PS XYZ:\> Set-CMClientStatusUpdateSchedule -Interval 23 -UnitType Hours
```

This command modifies the client status update schedule.

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

### -Interval
Specifies the number of hours or days between client status updates.

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

### -UnitType
Specifies whether the interval between schedule updates is calculated in hours or days.
Valid values are: Hours and Days.

```yaml
Type: ClientStatusUpdateScheduleUnit
Parameter Sets: (All)
Aliases:
Accepted values: Days, Hours

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

[How to Configure Client Status in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-client-status)

[Get-CMClientStatusUpdateSchedule](Get-CMClientStatusUpdateSchedule.md)

[Get-CMClientStatusSetting](Get-CMClientStatusSetting.md)

[Set-CMClientStatusSetting](Set-CMClientStatusSetting.md)


