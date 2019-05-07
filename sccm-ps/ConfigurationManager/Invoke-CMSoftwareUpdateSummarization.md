---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: C6C21CFF-2DF9-4D17-BC99-6367B2E90120
online version: https://go.microsoft.com/fwlink/?linkid=834173
schema: 2.0.0
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
The **Invoke-CMSoftwareUpdateSummarization** cmdlet runs the software update summarization in Microsoft System Center Configuration Manager immediately.
System Center Configuration Manager summarizes software update status on a regular schedule.
This cmdlet does not reset the time for the next automatic summarization.

You can use the Get-CMSoftwareUpdateSummarizationSchedule cmdlet to view the current schedule and the [Set-CMSoftwareUpdateSummarizationSchedule](Set-CMSoftwareUpdateSummarizationSchedule.md) cmdlet to change the schedule.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


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

[Get-CMSoftwareUpdateSummarizationSchedule](Get-CMSoftwareUpdateSummarizationSchedule.md)

[Set-CMSoftwareUpdateSummarizationSchedule](Set-CMSoftwareUpdateSummarizationSchedule.md)


