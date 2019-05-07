---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: 78F11C36-9204-405A-AB8C-4F4F305349EA
online version: https://go.microsoft.com/fwlink/?linkid=834202
schema: 2.0.0
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

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


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

[Set-CMClientStatusUpdateSchedule](Set-CMClientStatusUpdateSchedule.md)

[Get-CMClientStatusSetting](Get-CMClientStatusSetting.md)

[Set-CMClientStatusSetting](Set-CMClientStatusSetting.md)


