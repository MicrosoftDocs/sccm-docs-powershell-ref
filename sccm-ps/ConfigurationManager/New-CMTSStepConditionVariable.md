---
description: Create a condition variable on a task sequence step.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: New-CMTSStepConditionVariable
---

# New-CMTSStepConditionVariable

## SYNOPSIS

Create a condition variable on a task sequence step.

## SYNTAX

```
New-CMTSStepConditionVariable -ConditionVariableName <String> [-ConditionVariableValue <String>]
 -OperatorType <VariableOperatorType> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a condition variable on a task sequence step. The task sequence evaluates the variable value before it runs the step or group. For more information, see [How to use task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_access-condition).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Default condition

This example shows how to recreate the default condition on the **Restart in Windows PE** step in an imaging task sequence. It adds the following condition: `Task Sequence Variable _SMSTSInWinPE equals "false"`

It then adds the condition to a step named **Set Dynamic Variables** in the task sequence named **Default IPU**.

```powershell
$tscondition = New-CMTSStepConditionVariable -ConditionVariableName "_SMSTSInWinPE" -ConditionVariableValue "false" -OperatorType Equals

$tsname = "Default IPU"
$tsstep = "Set Dynamic Variables"

Set-CMTSStepSetDynamicVariable -TaskSequenceName $tsname -StepName $tsstep -AddCondition $tscondition
```

## PARAMETERS

### -ConditionVariableName

Specify the **Variable** name to evaluate. This variable name can be a built-in task sequence variable or a custom one that you created. For more information, see [How to use task sequence variables in Configuration Manager](/mem/configmgr/osd/understand/using-task-sequence-variables).

```yaml
Type: String
Parameter Sets: (All)
Aliases: Variable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionVariableValue

Specify the **Value** of the variable to evaluate in the condition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Value

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

### -OperatorType

Specify the **Condition** to evaluate the value of the variable in the condition.

```yaml
Type: VariableOperatorType
Parameter Sets: (All)
Aliases: Condition
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual, Like, NotLike

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

### IResultObject#SMS_TaskSequence_VariableConditionExpression
## NOTES

## RELATED LINKS

[Get-CMTaskSequenceStepCondition](Get-CMTaskSequenceStepCondition.md)

[New-CMTSStepConditionFile](New-CMTSStepConditionFile.md)
[New-CMTSStepConditionFolder](New-CMTSStepConditionFolder.md)
[New-CMTSStepConditionIfStatement](New-CMTSStepConditionIfStatement.md)
[New-CMTSStepConditionOperatingSystem](New-CMTSStepConditionOperatingSystem.md)
[New-CMTSStepConditionOperatingSystemLanguage](New-CMTSStepConditionOperatingSystemLanguage.md)
[New-CMTSStepConditionQueryWmi](New-CMTSStepConditionQueryWmi.md)
[New-CMTSStepConditionRegistry](New-CMTSStepConditionRegistry.md)
[New-CMTSStepConditionSoftware](New-CMTSStepConditionSoftware.md)
[New-CMTSStepConditionVariable](New-CMTSStepConditionVariable.md)

[How to use task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_access-condition)
