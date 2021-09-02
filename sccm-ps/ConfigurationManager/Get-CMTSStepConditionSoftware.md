---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# Get-CMTSStepConditionSoftware

## SYNOPSIS

Get an _installed software_ condition from a task sequence step.

## SYNTAX

```
Get-CMTSStepConditionSoftware -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a _installed software_ condition object from a task sequence step. You can use this object to:

- View the details of the condition on the step.
- Copy the condition to another task sequence step.

When you use the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets, provide this condition object with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: View the details of a software condition

This example first gets the **Default OS deployment** task sequence, then gets the **Set Dynamic Variables** step. It passes the task sequence step object to this cmdlet to view the condition details.

```powershell
$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsStepNameDynVar = "Set Dynamic Variables"
$tsStepDynVar = Get-CMTSStepSetDynamicVariable -InputObject $tsOsd -StepName $tsStepNameDynVar

Get-CMTSStepConditionSoftware -InputObject $tsStepDynVar
```

```output
SmsProviderObjectPath : SMS_TaskSequence_SoftwareConditionExpression
Operator              : ThisVersion
ProductCode           : {B3842C82-95EB-472C-940A-D82C4A10857D}
ProductName           : Microsoft Endpoint Configuration Manager Console
UpgradeCode           : {B038D5E8-6C93-4A05-9E21-240324CFDF0E}
Version               : 5.2107.1059.1000
```

### Example 2: Copy a condition to another step

This example first gets the **Default OS deployment** task sequence, then gets the **Set Dynamic Variables** step. It passes the task sequence step object to this cmdlet and saves the object in the **$condition** variable.

It then uses the **Set-CMTSStepSetVariable** cmdlet with the **AddCondition** parameter to add this same condition to the **Set Task Sequence Variable** step.

```powershell
$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsStepNameDynVar = "Set Dynamic Variables"
$tsStepDynVar = Get-CMTSStepSetDynamicVariable -InputObject $tsOsd -StepName $tsStepNameDynVar

$condition = Get-CMTSStepConditionSoftware -InputObject $tsStepDynVar

$tsStepNameSetTSVar = "Set Task Sequence Variable"

Set-CMTSStepSetVariable -TaskSequenceName $tsNameOsd -StepName $tsStepNameSetTSVar -AddCondition $condition
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

Specify a task sequence step object with a software condition. To get this object, use one of the **Get-CMTSStep** cmdlets. For example, [Get-CMTSStepApplyDataImage](Get-CMTSStepApplyDataImage.md).

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

### IResultObject[]#SMS_TaskSequence_SoftwareConditionExpression

### IResultObject#SMS_TaskSequence_SoftwareConditionExpression

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_SoftwareConditionExpression server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_softwareconditionexpression-server-wmi-class).

## RELATED LINKS

[New-CMTSStepConditionSoftware](New-CMTSStepConditionSoftware.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
