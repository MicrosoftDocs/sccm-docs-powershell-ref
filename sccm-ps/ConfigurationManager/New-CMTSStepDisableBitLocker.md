---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/12/2021
online version:
schema: 2.0.0
---

# New-CMTSStepDisableBitLocker

## SYNOPSIS

Create an **Disable BitLocker** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepDisableBitLocker [-Drive <String>] [-RebootCount <Int32>] [-Condition <IResultObject[]>]
 [-ContinueOnError] [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Disable BitLocker** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Disable BitLocker](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_DisableBitLocker).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example creates an object for the **Disable BitLocker** step, which keeps BitLocker disabled until the computer has restarted 12 times. Since a drive letter isn't specified, it disables BitLocker on the current OS drive.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$step = New-CMTSStepDisableBitLocker -Name "Disable BitLocker" -RebootCount 12

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

### -Drive

Specify the drive letter to disable BitLocker on a specific drive. If you don't specify this parameter, the step disables BitLocker on the current OS drive.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpecificDrive

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

### -RebootCount

Use this parameter to resume protection after Windows has been restarted the specified number of times. Instead of adding multiple instances of this step, set a value between `1` (default) and `15`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RebootNumber

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

### IResultObject#SMS_TaskSequence_DisableBitLockerAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_DisableBitLockerAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_disablebitlockeraction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepDisableBitLocker](Get-CMTSStepDisableBitLocker.md)
[Remove-CMTSStepDisableBitLocker](Remove-CMTSStepDisableBitLocker.md)
[Set-CMTSStepDisableBitLocker](Set-CMTSStepDisableBitLocker.md)

[About task sequence steps: Disable BitLocker](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_DisableBitLocker)
