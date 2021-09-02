---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/01/2021
online version:
schema: 2.0.0
---

# New-CMTSStepSetDynamicVariable

## SYNOPSIS

Create a **Set Dynamic Variables** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepSetDynamicVariable -AddRule <IResultObject[]> [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Set Dynamic Variables** step object. Use the [New-CMTSRule](New-CMTSRule.md) cmdlet to define the rules for this step. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Set Dynamic Variables](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetDynamicVariables).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **New-CMTSRule** cmdlet to create two rules.

It then creates an object for the **Set Dynamic Variables** step, and adds this rule.

Finally, it gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$tsrule1 = New-CMTSRule -Variable @{'OSDDownloadDestinationLocationType' = 'TSCache'} -ReferencedVariableName "_SMSTSInWinPE" -ReferencedVariableOperator Equals -ReferencedVariableValue TRUE

$tsrule2 = New-CMTSRule -Variable @{'OSDMigrateUseHardlinks' = 'true'} -ReferencedVariableName "_SMSTSMediaType" -ReferencedVariableOperator NotEquals -ReferencedVariableValue "OEMMedia"

$step = New-CMTSStepSetDynamicVariable -Name "Set Dynamic Variables" -AddRule $tsrule1,$tsrule2

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -AddRule

Specify one or more rule objects. Rules define the criteria and variables to set when they evaluate true. To get this object, use the [New-CMTSRule](New-CMTSRule.md) cmdlet. The order of the rules in the array determines the order in this step.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddRules

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### IResultObject#SMS_TaskSequence_SetDynamicVariablesAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_SetDynamicVariablesAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_setdynamicvariablesaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepSetDynamicVariable](Get-CMTSStepSetDynamicVariable.md)
[Remove-CMTSStepSetDynamicVariable](Remove-CMTSStepSetDynamicVariable.md)
[Set-CMTSStepSetDynamicVariable](Set-CMTSStepSetDynamicVariable.md)

[New-CMTSRule](New-CMTSRule.md)

[About task sequence steps: Set Dynamic Variables](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetDynamicVariables)
