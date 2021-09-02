---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionIfStatement

## SYNOPSIS

Create an _if statement_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionIfStatement [-Condition <IResultObject[]>] -StatementType <ConditionStatementType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an _if statement_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **New-CMTSStepConditionFile** and **New-CMTSStepConditionQueryWMI** cmdlets to create child condition objects. It passes those two objects to the **New-CMTSStepConditionIfStatement** cmdlet and saves that condition object.

It then uses the **Set-CMTSStepSetDynamicVariable** cmdlet to add this condition object to the **Set Dynamic Variables** step of the **Default OS deployment** task sequence.

```powershell
$file = "C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\en-US\AdminUI.PS.dll-Help.xml"
$datetime = Get-Date ("August 2, 2021")
$conditionFile = New-CMTSStepConditionFile -FilePath $file -FileTimestamp $datetime -FileDateTimeOperator Greater

$model = "Latitude E7470"
$wmiQuery = "Select * From Win32_ComputerSystem Where Model = `"$Model`""
$conditionQuery = New-CMTSStepConditionQueryWMI -Namespace "root\cimv2" -Query $wmiQuery

$condition = New-CMTSStepConditionIfStatement -StatementType All -Condition $conditionFile,$conditionQuery

$tsNameOsd = "Default OS deployment"
$tsStepNameSetDynVar = "Set Dynamic Variables"

Set-CMTSStepSetDynamicVariable -TaskSequenceName $tsNameOsd -StepName $tsStepNameSetDynVar -AddCondition $condition
```

```
If  All  the conditions are true:
    File  C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\en-US\AdminUI.PS.dll-Help.xml exists  and  timestamp greater than "8/1/2021 16:00:00"
    WMI Query  Select * From Win32_ComputerSystem Where Model = "Latitude E7470"
```

## PARAMETERS

### -Condition

Specify one or more condition objects to include in this _if statement_ block. To get these nested objects, use one of the **New-CMTSStepCondition\*** cmdlets. For example, [New-CMTSStepConditionFile](New-CMTSStepConditionFile.md).

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SubCondition, SubConditions

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

### -StatementType

Specify the type of _if statement_ to create. There are three types of checks that you can do with this condition:

- If `All` of the conditions are true
- If `Any` of the conditions are true
- If `None` of the conditions are true

```yaml
Type: ConditionStatementType
Parameter Sets: (All)
Aliases: Operator
Accepted values: All, Any, None

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

### IResultObject#SMS_TaskSequence_ConditionOperator

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_ConditionOperator server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_conditionoperator-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepConditionIfStatement](Get-CMTSStepConditionIfStatement.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
