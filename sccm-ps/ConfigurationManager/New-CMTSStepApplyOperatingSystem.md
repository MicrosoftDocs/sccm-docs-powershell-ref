---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
online version:
schema: 2.0.0
---

# New-CMTSStepApplyOperatingSystem

## SYNOPSIS

Create an **Apply OS Image** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepApplyOperatingSystem [-ConfigFileName <String>] [-ConfigFilePackage <IResultObject>]
 [-Destination <DestinationType>] [-DestinationDisk <Int32>] [-DestinationDriveLetter <String>]
 [-LayeredDriver <OsdLayeredDriver>] [-DestinationPartition <Int32>] [-DestinationVariable <String>]
 [-ImagePackage <IResultObject>] [-ImagePackageIndex <Int32>] [-InstallPackage <IResultObject>]
 [-InstallPackageIndex <Int32>] [-RunFromNet <Boolean>] [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Apply OS Image** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Apply OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyOperatingSystemImage).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMOperatingSystemImage** cmdlet to get an object for the OS image package. It saves this object in the **$osImgPkg** variable. The next step creates an object for the **Apply OS Image** step, using the **$osImgPkg** object as the image package.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$osImgPkg = Get-CMOperatingSystemImage -Name "OSImagePkg01"
$step = New-CMTSStepApplyOperatingSystem -Name "Apply OS image" -ImagePackage $osImgPkg -ImagePackageIndex 1

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

### -ConfigFileName

Specify the file name of an unattended or Sysprep answer file to use for a custom installation. Use this parameter with the **ConfigFilePackage** parameter.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AnswerFileName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigFilePackage

Specify a package object that includes the unattended or Sysprep answer file to use for a custom installation. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet. Use this parameter with the **ConfigFileName** parameter.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: AnswerFilePackage

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

### -Destination

Specify the location where you want to apply this OS. If you don't specify this parameter, the default is `NextAvailableFormattedPartition`.

- `NextAvailableFormattedPartition`: Use the next sequential partition not already targeted by an **Apply Operating System** or **Apply Data Image** step in this task sequence.

- `SpecificDiskAndPartition`: Specify the disk number with the **DestinationDisk** parameter and the partition number with the **DestinationPartition** parameter.

- `SpecificLogicalDriverLetter`: Use the **DestinationDriveLetter** parameter to specify the logical drive letter assigned to the partition by Windows PE. This drive letter can be different from the drive letter assigned by the newly deployed OS.

- `LogicalDriverLetterInVariable`: Use the **DestinationVariable** parameter to specify the task sequence variable containing the drive letter assigned to the partition by Windows PE. This variable is typically set with the **DiskNumberVariable** parameter of the [Set-CMTSStepPartitionDisk](Set-CMTSStepPartitionDisk.md) or [New-CMTSStepPartitionDisk](New-CMTSStepPartitionDisk.md) cmdlets for the **Format and Partition Disk** task sequence step.

```yaml
Type: DestinationType
Parameter Sets: (All)
Aliases:
Accepted values: NextAvailableFormattedPartition, SpecificDiskAndPartition, SpecificLogicalDriverLetter, LogicalDriverLetterInVariable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationDisk

When you use `-Destination SpecificDiskAndPartition`, use this parameter to specify the disk number. Specify an integer from `0` to `99`. Also use the **DestinationPartition** parameter.

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

### -DestinationDriveLetter

When you use `-Destination SpecificLogicalDriverLetter`, use this parameter to specify the logical drive letter. Specify a drive letter from `C` to `Z`.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DestinationLogicalDrive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPartition

When you use `-Destination SpecificDiskAndPartition`, use this parameter to specify the partition number. Specify an integer from `1` to `99`. Also use the **DestinationDisk** parameter.

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

### -DestinationVariable

When you use `-Destination LogicalDriverLetterInVariable`, use this parameter to specify the task sequence variable with the logical drive letter. The variable name needs to alphanumeric without spaces and fewer than 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DestinationVariableName

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

### -ImagePackage

Specify an OS image package object. The step applies the OS from this image. Use the **ImagePackageIndex** parameter to set the image index.

To get this object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImagePackageIndex

Specify an integer value of the image index. Use this parameter with the **ImagePackage** parameter.

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

### -InstallPackage

Specify an OS upgrade package object. The step applies the OS from this original installation source. Use the **InstallPackageIndex** parameter to set the edition.

To get this object, use the [Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: UpgradePackage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallPackageIndex

Specify an integer value of the OS upgrade package edition. Use this parameter with the **InstallPackage** parameter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: UpgradePackageIndex

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

### -RunFromNet

Set this parameter to `$true` to allow the task sequence to apply the OS image directly from the distribution point.

For greatest security, it's recommended to not enable this setting. This option is designed for use on devices with limited storage capacity. For more information, see [Access content directly from the distribution point](/mem/configmgr/osd/understand/task-sequence-steps#access-content-directly-from-the-distribution-point).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowAccessFromDistributionPoint

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

### -LayeredDriver

Starting in version 2107, use this parameter to select other types of keyboards that are common with Japanese and Korean languages. Specify an integer value for the layered driver to install with Windows. Use the same values as the [OsdLayeredDriver](/mem/configmgr/osd/understand/task-sequence-variables#OsdLayeredDriver) task sequence variable.

```yaml
Type: OsdLayeredDriver
Parameter Sets: (All)
Aliases: KeyboardDriver

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

### IResultObject#SMS_TaskSequence_ApplyOperatingSystemAction
## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_ApplyOperatingSystemAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_applyoperatingsystemaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepApplyOperatingSystem](Get-CMTSStepApplyOperatingSystem.md)
[Remove-CMTSStepApplyOperatingSystem](Remove-CMTSStepApplyOperatingSystem.md)
[Set-CMTSStepApplyOperatingSystem](Set-CMTSStepApplyOperatingSystem.md)

[About task sequence steps: Apply OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyOperatingSystemImage)
