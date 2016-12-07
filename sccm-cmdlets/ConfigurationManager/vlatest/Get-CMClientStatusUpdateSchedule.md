---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834202
schema: 2.0.0
ms.assetid: 78F11C36-9204-405A-AB8C-4F4F305349EA
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

## EXAMPLES

### Example 1: Gets a client status update schedule
```
PS C:\>Get-CMClientStatusUpdateSchedule
Interval Unit 
-------- ----
       1 Days
```

This command gets a client status update schedule.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMClientStatusUpdateSchedule](./Set-CMClientStatusUpdateSchedule.md)

[Get-CMClientStatusSetting](./Get-CMClientStatusSetting.md)

[Set-CMClientStatusSetting](./Set-CMClientStatusSetting.md)


