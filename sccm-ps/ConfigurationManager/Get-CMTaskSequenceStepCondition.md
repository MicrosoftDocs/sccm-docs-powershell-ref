---
description: Get a condition on a task sequence step.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/30/2018
schema: 2.0.0
title: Get-CMTaskSequenceStepCondition
---

# Get-CMTaskSequenceStepCondition

## SYNOPSIS

Get a condition on a task sequence step.

## SYNTAX

```
Get-CMTaskSequenceStepCondition -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a condition on a task sequence step. The task sequence evaluates the condition before it runs the step or group. For more information, see [How to use task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_access-condition).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a default condition

This example shows how to get the default condition on the **Post-Processing** group of an in-place upgrade task sequence.

```powershell
$tsname = "Default IPU"
$tsgroup = "Post-Processing"
$ts = Get-CMTaskSequence -Name $tsname

$ts | Get-CMTaskSequenceGroup -StepName $tsgroup | Get-CMTaskSequenceStepCondition
```

```output
SmsProviderObjectPath : SMS_TaskSequence_VariableConditionExpression
Operator              : equals
Value                 : false
Variable              : _SMSTSSetupRollback
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

### -InputObject

Specify a task sequence group or step object. To get this object, use the [Get-CMTaskSequenceGroup](Get-CMTaskSequenceGroup.md) or [Get-CMTaskSequenceStep](Get-CMTaskSequenceStep.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: TaskSequenceStep

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_TaskSequence_Condition
### IResultObject#SMS_TaskSequence_Condition
## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_Condition server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_condition-server-wmi-class).

## RELATED LINKS

[Get-CMTaskSequenceStep](./Get-CMTaskSequenceStep.md)

[Get-CMTaskSequenceGroup](./Get-CMTaskSequenceGroup.md)
