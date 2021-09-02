---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/01/2021
online version:
schema: 2.0.0
---

# New-CMTSStepSetVariable

## SYNOPSIS

Create a **Set Task Sequence Variable** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepSetVariable [-IsMasked <Boolean>] -TaskSequenceVariable <String>
 [-TaskSequenceVariableValue <String>] [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Set Task Sequence Variable** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Set Task Sequence Variable](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetTaskSequenceVariable).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first creates an object for the **Set Task Sequence Variable** step, to set the **OSDSetupAdditionalUpgradeOptions** built-in variable to **/ReflectDrivers**.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$step = New-CMTSStepSetVariable -Name "Set Task Sequence Variable" -TaskSequenceVariable "OSDSetupAdditionalUpgradeOptions" -TaskSequenceVariableValue "/ReflectDrivers"

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

### -IsMasked

Set this parameter to `$true` to mask sensitive data stored in task sequence variables. For example, when specifying a password.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: IsHidden, IsMask

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

### -TaskSequenceVariable

Specify the name of a task sequence built-in or action variable, or specify your own user-defined variable name. For more information, see [How to use task sequence variables in Configuration Manager](/mem/configmgr/osd/understand/using-task-sequence-variables) and the reference of [Task sequence variables](/mem/configmgr/osd/understand/task-sequence-variables).

Use the **TaskSequenceVariableValue** parameter to set the value.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VariableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceVariableValue

The task sequence sets the **TaskSequenceVariable** to this value. Set this task sequence variable to the value of another task sequence variable with the syntax `%varname%`.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VariableValue

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

### IResultObject#SMS_TaskSequence_SetVariableAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_SetVariableAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_setvariableaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepSetVariable](Get-CMTSStepSetVariable.md)
[Remove-CMTSStepSetVariable](Remove-CMTSStepSetVariable.md)
[Set-CMTSStepSetVariable](Set-CMTSStepSetVariable.md)

[About task sequence steps: Set Task Sequence Variable](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetTaskSequenceVariable)
