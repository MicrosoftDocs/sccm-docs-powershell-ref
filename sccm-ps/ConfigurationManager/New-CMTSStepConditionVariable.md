---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionVariable

## SYNOPSIS

Create a _task sequence variable_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionVariable -ConditionVariableName <String> [-ConditionVariableValue <String>]
 -OperatorType <VariableOperatorType> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a _task sequence variable_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

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

Specify the name of the task sequence variable to evaluate. This variable name can be a built-in task sequence variable or a custom one that you created. For more information, see the reference of [Task sequence variables in Configuration Manager](/mem/configmgr/osd/understand/task-sequence-variables).

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

If you use a comparative **OperatorType** like `Equals`, then specify the value of the variable to evaluate in the condition.

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

Specify the operator type to evaluate the value of the variable in the condition. If you use `Exists` or `NotExists`, then the **ConditionVariableValue** parameter isn't required. For the other comparative operator types, use the **ConditionVariableValue** parameter to specify the value to compare.

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

For more information on this return object and its properties, see [SMS_TaskSequence_VariableConditionExpression server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_variableconditionexpression-server-wmi-class).

## RELATED LINKS

[Get-CMTaskSequenceStepCondition](Get-CMTaskSequenceStepCondition.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)

[How to access variables in a step condition](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_access-condition)
