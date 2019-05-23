---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: 62D4DFB1-3F7B-49A2-AEA8-8FA5747B743F
online version: https://go.microsoft.com/fwlink/?linkid=833929
schema: 2.0.0
---

# Get-CMSoftwareUpdateSummarizationSchedule

## SYNOPSIS
Displays the Configuration Manager schedule for software update summarization.

## SYNTAX

```
Get-CMSoftwareUpdateSummarizationSchedule [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateSummarizationSchedule** cmdlet displays the current schedule for software update summarization for Microsoft System Center Configuration Manager.
You can use the [Set-CMSoftwareUpdateSummarizationSchedule](Set-CMSoftwareUpdateSummarizationSchedule.md) cmdlet to change the schedule.
You can use the [Invoke-CMSoftwareUpdateSummarization](Invoke-CMSoftwareUpdateSummarization.md) cmdlet to run the summarization immediately.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Display the summarization schedule
```
PS XYZ:\> Get-CMSoftwareUpdateSummarizationSchedule
                               Interval                                    Unit
                               --------                                    ----
                                     12                                   Hours
```

This command displays the summarization schedule for software updates.
In this case, the schedule is every 12 hours.

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

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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

[Set-CMSoftwareUpdateSummarizationSchedule](Set-CMSoftwareUpdateSummarizationSchedule.md)

[Invoke-CMSoftwareUpdateSummarization](Invoke-CMSoftwareUpdateSummarization.md)
