---
description: Creates a t s step partition disk.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/29/2020
schema: 2.0.0
title: New-CMTSStepPartitionDisk
---

# New-CMTSStepPartitionDisk

## SYNOPSIS
Add the **Format and Partition Disk** step in a task sequence.

## SYNTAX

```
New-CMTSStepPartitionDisk [-DiskNumber <Int32>] [-DiskNumberVariable <String>] [-DiskType <PartitionDiskStyle>]
 [-IsBootDisk <Boolean>] -PartitionSetting <IResultObject[]> [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Add the **Format and Partition Disk** step in a task sequence. For more information on this task sequence step, see [About task sequence steps](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

{{ Add example description here }}

```powershell
{{ Add example code here }}
```

## PARAMETERS

### -Condition

Specify a condition object to add to this step.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Conditions

Required: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinueOnError

Add this parameter to enable the step option **Continue on error**. When you enable this option, if the step fails, the task sequence continues.

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

### -Description

Specify an optional description for this task sequence step.

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

### -Disable

Add this parameter to disable this task sequence step.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableThisStep

Required: False
Position: Named
Default value: None
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

### -DiskNumber

Specify an integer for the physical disk number of the disk to format. The number is based on Windows disk enumeration ordering.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskNumberVariable

Applies to version 2006 and later. Use a task sequence variable to specify the target disk to format. This variable option supports more complex task sequences with dynamic behaviors. For more information, see [About task sequence steps - Format and Parition Disk](/mem/configmgr/osd/understand/task-sequence-steps#properties-for-format-and-partition-disk).

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

### -DiskType

Specify the type of the disk to format:

- `Mbr`: Master Boot Record
- `Gpt`: GUID Partition Table

```yaml
Type: PartitionDiskStyle
Parameter Sets: (All)
Aliases:
Accepted values: Mbr, Gpt

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

### -IsBootDisk

For a new partition, set this parameter to `true` to make it the boot partition.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify a name for this step to identify it in the task sequence.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionSetting

Specify an array of partition setting objects.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: PartitionSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. It doesn't run the cmdlet.

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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_PartitionDiskAction

## NOTES

## RELATED LINKS

[About task sequence steps - Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk)
