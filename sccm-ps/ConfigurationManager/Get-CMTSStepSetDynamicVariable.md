---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 09/01/2021
online version:
schema: 2.0.0
---

# Get-CMTSStepSetDynamicVariable

## SYNOPSIS

Get the **Set Dynamic Variables** step from a specific task sequence.

## SYNTAX

### ByValue (Default)
```
Get-CMTSStepSetDynamicVariable [-InputObject] <IResultObject> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Get-CMTSStepSetDynamicVariable [-TaskSequenceId] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Get-CMTSStepSetDynamicVariable [-TaskSequenceName] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a task sequence step object for one or more instances of the **Set Dynamic Variables** step. You can use this object to:

- Remove the step from a task sequence with [Remove-CMTSStepSetDynamicVariable](Remove-CMTSStepSetDynamicVariable.md)
- Copy the step to another task sequence with [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md)

For more information on this step, see [About task sequence steps: Set Dynamic Variables](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets a task sequence object in the **$tsOsd** variable. It then passes that variable as the input object to get the **Set Dynamic Variables** step.

```powershell
$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsStepNameDynVar = "Set Dynamic Variables"
$tsStepDynVar = Get-CMTSStepSetDynamicVariable -InputObject $tsOsd -StepName $tsStepNameDynVar
```

## PARAMETERS

### -InputObject

Specify a task sequence object from which to get the **Set Dynamic Variables** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StepName

Specify the name of the **Set Dynamic Variables** step to get from the task sequence.

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

### -TaskSequenceId

Specify the **package ID** of the task sequence from which to get the **Set Dynamic Variables** step. This value is a standard package ID, for example `XYZ00858`.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id, TaskSequencePackageId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify the name of the task sequence from which to get the **Set Dynamic Variables** step.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[New-CMTSStepSetDynamicVariable](New-CMTSStepSetDynamicVariable.md)
[Remove-CMTSStepSetDynamicVariable](Remove-CMTSStepSetDynamicVariable.md)
[Set-CMTSStepSetDynamicVariable](Set-CMTSStepSetDynamicVariable.md)

[About task sequence steps: Set Dynamic Variables](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetDynamicVariables)
