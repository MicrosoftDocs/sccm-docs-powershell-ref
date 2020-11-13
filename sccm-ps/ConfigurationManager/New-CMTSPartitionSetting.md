---
description: Create a task sequence partition setting.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/30/2020
online version:
schema: 2.0.0
---

# New-CMTSPartitionSetting

## SYNOPSIS

Create a task sequence partition object to use with the **Format and Partition Disk** step.

## SYNTAX

### PrimaryPartition (Default)
```
New-CMTSPartitionSetting [-EnableDriveLetterAssignment <Boolean>] [-EnableQuickFormat <Boolean>]
 [-IsBootPartition <Boolean>] [-Name <String>] [-PartitionFileSystem <FileSystemType>] [-PartitionPrimary]
 [-Size <Int32>] [-SizeUnit <SizeUnitType>] [-Variable <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EfiPartition
```
New-CMTSPartitionSetting [-Name <String>] [-PartitionEfi] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExtendedPartition
```
New-CMTSPartitionSetting [-Name <String>] [-PartitionExtended] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HiddenPartition
```
New-CMTSPartitionSetting [-Name <String>] [-PartitionHidden] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LogicalPartition
```
New-CMTSPartitionSetting [-Name <String>] [-PartitionLogical] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MsrPartition
```
New-CMTSPartitionSetting [-Name <String>] [-PartitionMsr] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecoveryPartition
```
New-CMTSPartitionSetting [-Name <String>] [-PartitionRecovery] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a task sequence partition object to use with the **Format and Partition Disk** step. Use this cmdlet to define the partition settings, and then use that object with the **-PartitionSetting** parameter of the [New-CMTSStepPartitionDisk](new-cmtssteppartitiondisk.md) or [Set-CMTSStepPartitionDisk](set-cmtssteppartitiondisk.md) cmdlets.

This cmdlet corresponds to the new **Partition Properties** window from the [Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk) step in the task sequence editor.

## EXAMPLES

### Example 1

{{ Add example description here }}

```powershell
{{ Add example code here }}
```

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

### -EnableDriveLetterAssignment

Set this parameter to `true` to let Configuration Manager assign a drive letter to the partition.

```yaml
Type: Boolean
Parameter Sets: PrimaryPartition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableQuickFormat

Set this parameter to `true` to let Configuration Manager do a quick format of the partition.

```yaml
Type: Boolean
Parameter Sets: PrimaryPartition
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

### -IsBootPartition

Set this parameter to `true` to make this partition the boot partition.

```yaml
Type: Boolean
Parameter Sets: PrimaryPartition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify a name for the partition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PartitionName, VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionEfi

Add this parameter to make the partition type **EFI**.

```yaml
Type: SwitchParameter
Parameter Sets: EfiPartition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionExtended

Add this parameter to make the partition type **Extended**.

```yaml
Type: SwitchParameter
Parameter Sets: ExtendedPartition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionFileSystem

Specify the file system to format the partition.

```yaml
Type: FileSystemType
Parameter Sets: PrimaryPartition
Aliases:
Accepted values: Ntfs, Fat32

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionHidden

Add this parameter to make the partition type **Hidden**.

```yaml
Type: SwitchParameter
Parameter Sets: HiddenPartition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionLogical

Add this parameter to make the partition type **Logical**.

```yaml
Type: SwitchParameter
Parameter Sets: LogicalPartition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionMsr

Add this parameter to make the partition type **MSR**.

```yaml
Type: SwitchParameter
Parameter Sets: MsrPartition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionPrimary

Add this parameter to make the partition type **Primary**.

```yaml
Type: SwitchParameter
Parameter Sets: PrimaryPartition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionRecovery

Add this parameter to make the partition type **Recovery**.

```yaml
Type: SwitchParameter
Parameter Sets: RecoveryPartition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Size

Specify an integer value for the size of the partition. Use this parameter with the **-SizeUnit** parameter. If **-SizeUnit** is `Percent`, then specify a number between 1-100 for this parameter. If **-SizeUnit** is `MB` or `GB`, specify a number for the specific partition size.

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

### -SizeUnit

Specify the unit type for the size. Use this parameter with the **-Size** parameter.

- `Percent`: Use **-Size** to set the partition to a percentage of remaining free space on the disk.

- `MB` or `GB`: Use **-Size** to set a specific size for the partition.

```yaml
Type: SizeUnitType
Parameter Sets: (All)
Aliases:
Accepted values: MB, GB, Percent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable

By default, Configuration Manager assigns the next available drive letter to this partition. To save this drive letter for future use, set a custom task sequence variable with this parameter.

```yaml
Type: String
Parameter Sets: PrimaryPartition
Aliases:

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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_PartitionSettings

## NOTES

## RELATED LINKS

[New-CMTSStepPartitionDisk](new-cmtssteppartitiondisk.md)

[Set-CMTSStepPartitionDisk](set-cmtssteppartitiondisk.md)

[About task sequence steps - Format and Partition Disk](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk)

[UEFI/GPT-based hard drive partitions](/windows-hardware/manufacture/desktop/configure-uefigpt-based-hard-drive-partitions)

[BIOS/MBR-based hard drive partitions](/windows-hardware/manufacture/desktop/configure-biosmbr-based-hard-drive-partitions)
