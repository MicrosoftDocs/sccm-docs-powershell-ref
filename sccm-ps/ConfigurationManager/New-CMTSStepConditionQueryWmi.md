---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionQueryWmi

## SYNOPSIS

Create a _WMI query_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionQueryWmi [-Namespace <String[]>] -Query <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a _WMI query_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a query condition based on hardware model

This example first creates a condition object to query WMI for the computer model.

It then uses the **Set-CMTSStepRunPowerShellScript** cmdlet to add this condition object to the **Run PowerShell Script** step of the **Default OS deployment** task sequence.

```powershell
$model = "Latitude E7470"
$query = "Select * From Win32_ComputerSystem Where Model = `"$model`""

$condition = New-CMTSStepConditionQueryWMI -Namespace "root\cimv2" -Query $query

$tsNameOsd = "Default OS deployment"
$tsStepNameRunPwsh = "Run PowerShell Script"

Set-CMTSStepRunPowerShellScript -TaskSequenceName $tsNameOsd -StepName $tsStepNameRunPwsh -AddCondition $condition
```

This sample script creates the following condition on the step:

`WMI Query  Select * From Win32_ComputerSystem Where Model = "Latitude E7470"`

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

### -Namespace

Specify the WMI namespace for the query. For example, `root\cimv2`

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query

Specify the WMI query. The cmdlet doesn't test the validity of the query.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

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

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

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

### IResultObject#SMS_TaskSequence_WMIConditionExpression

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_WMIConditionExpression server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_wmiconditionexpression-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepConditionQueryWmi](Get-CMTSStepConditionQueryWmi.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
