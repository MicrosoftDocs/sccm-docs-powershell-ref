---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2021
schema: 2.0.0
title: Get-CMTSStepPartitionDisk
---

# Get-CMTSStepPartitionDisk

## SYNOPSIS

Get the **Format and Partition Disk** step from a specific task sequence.

## SYNTAX

### ByValue (Default)
```
Get-CMTSStepPartitionDisk [-InputObject] <IResultObject> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Get-CMTSStepPartitionDisk [-TaskSequenceId] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Get-CMTSStepPartitionDisk [-TaskSequenceName] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a task sequence step object for one or more instances of the **Format and Partition Disk** step. You can use this object to:

- Remove the step from a task sequence with [Remove-CMTSStepPartitionDisk](Remove-CMTSStepPartitionDisk.md)
- Copy the step to another task sequence with [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md)

For more information on this step, see [About task sequence steps: Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the step from a task sequence

This example first gets a task sequence object in the **$tsOsd** variable. It then passes that variable as the input object to get the **Format and Partition Disk** step.

```powershell
$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsStepNameFormatDisk = "Partition Disk 0 - UEFI"
$tsStepFormatDisk = Get-CMTSStepPartitionDisk -InputObject $tsOsd -StepName $tsStepNameFormatDisk
```

### Example 2: View the partition setting details for a step

This example builds on the previous example. To view the first partition settings, reference the **Partitions** property, which is an array of [SMS_TaskSequence_PartitionSettings](/mem/configmgr/develop/reference/osd/sms_tasksequence_partitionsettings-server-wmi-class) objects.

```powershell
$tsStepFormatDisk = Get-CMTSStepPartitionDisk -InputObject $tsOsd -StepName $tsStepNameFormatDisk

$tsStepFormatDisk.Partitions[0]
```

You can use this process to copy partition settings between steps or task sequences. Save this partition settings object as a variable and then add it to another step.

## PARAMETERS

### -InputObject

Specify a task sequence object from which to get the **Format and Partition Disk** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StepName

Specify the name of the **Format and Partition Disk** step to get from the task sequence.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceId

Specify the **package ID** of the task sequence from which to get the **Format and Partition Disk** step. This value is a standard package ID, for example `XYZ00858`.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id, TaskSequencePackageId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify the name of the task sequence from which to get the **Format and Partition Disk** step.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[New-CMTSStepPartitionDisk](New-CMTSStepPartitionDisk.md)
[Remove-CMTSStepPartitionDisk](Remove-CMTSStepPartitionDisk.md)
[Set-CMTSStepPartitionDisk](Set-CMTSStepPartitionDisk.md)

[New-CMTSPartitionSetting](New-CMTSPartitionSetting.md)

[About task sequence steps: Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk)
