---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833726
schema: 2.0.0
ms.assetid: 6ABB57F2-9CCE-420E-8ECA-01AB5C8B0A50
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
For more information, see [How to Configure Client Status in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=247263) on TechNet.

## EXAMPLES

### Example 1: Modify a client's status update schedule
```
PS C:\> Set-CMClientStatusUpdateSchedule -Interval 23 -UnitType Hours
```

This command modifies the client status update schedule.

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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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

[How to Configure Client Status in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=247263)

[Get-CMClientStatusUpdateSchedule](./Get-CMClientStatusUpdateSchedule.md)

[Get-CMClientStatusSetting](./Get-CMClientStatusSetting.md)

[Set-CMClientStatusSetting](./Set-CMClientStatusSetting.md)


