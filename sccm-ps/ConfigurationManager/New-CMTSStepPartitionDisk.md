---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2021
schema: 2.0.0
title: New-CMTSStepPartitionDisk
---

# New-CMTSStepPartitionDisk

## SYNOPSIS

Create the **Format and Partition Disk** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepPartitionDisk [-DiskNumber <Int32>] [-DiskNumberVariable <String>] [-DiskType <PartitionDiskStyle>]
 [-IsBootDisk <Boolean>] -PartitionSetting <IResultObject[]> [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Format and Partition Disk** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first creates four partition setting objects, which are the default partitions for a UEFI disk.

It then creates an object for the **Format and Partition Disk** step, using the partition settings and other typical configurations for a UEFI disk.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$partEfi = New-CMTSPartitionSetting -Name "EFI" -PartitionEfi -Size 500 -SizeUnit MB
$partMsr = New-CMTSPartitionSetting -Name "MSR" -PartitionMsr -Size 128 -SizeUnit MB
$partWin = New-CMTSPartitionSetting -Name "Windows" -PartitionPrimary -Size 99 -SizeUnit Percent -EnableDriveLetterAssignment $true -EnableQuickFormat $true -PartitionFileSystem NTFS -IsBootPartition $true
$partRec = New-CMTSPartitionSetting -Name "Recovery" -PartitionRecovery -Size 100 -SizeUnit Percent 

$step = New-CMTSStepPartitionDisk -Name "Partition Disk 0 - UEFI" -PartitionSetting @($partEfi,$partMsr,$partWin,$partRec) -DiskNumber 0 -DiskType Gpt -IsBootDisk $true

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -Condition

Specify a condition object to use with this step. To get this object, use one of the task sequence condition cmdlets. For example, [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md).

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

Specify an array of partition setting objects. To get this object, use the [New-CMTSPartitionSetting](New-CMTSPartitionSetting.md) cmdlet.

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

For more information on this return object and its properties, see [SMS_TaskSequence_PartitionDiskAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_partitiondiskaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepPartitionDisk](Get-CMTSStepPartitionDisk.md)
[Remove-CMTSStepPartitionDisk](Remove-CMTSStepPartitionDisk.md)
[Set-CMTSStepPartitionDisk](Set-CMTSStepPartitionDisk.md)

[New-CMTSPartitionSetting](New-CMTSPartitionSetting.md)

[About task sequence steps: Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk)
