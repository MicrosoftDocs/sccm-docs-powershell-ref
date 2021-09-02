---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionFolder

## SYNOPSIS

Create a _folder properties_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionFolder [-FolderDateTimeOperator <VariableOperatorType>] -FolderPath <String>
 [-FolderTimestamp <DateTime>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a _folder properties_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

There are two types of checks that you can do with this condition:

- To check if the folder exists, use the required **FolderPath** parameter.
- To also check the folder timestamp, use the **FolderTimestamp** and **FolderDateTimeOperator** parameters.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example checks for the existence and timestamp for the Configuration Manager PowerShell module help file folder. It creates a condition object for the folder and that its timestamp is greater than August 2, 2021.

It then uses the **Set-CMTSStepRunPowerShellScript** cmdlet to add this condition object to the **Run PowerShell Script** step of the **Default OS deployment** task sequence.

```powershell
$folder = "C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\en-US"
$datetime = Get-Date ("August 2, 2021")

$condition = New-CMTSStepConditionFolder -FolderPath $folder -FolderTimestamp $datetime -FolderDateTimeOperator Greater

$tsNameOsd = "Default OS deployment"
$tsStepNameRunPwsh = "Run PowerShell Script"

Set-CMTSStepRunPowerShellScript -TaskSequenceName $tsNameOsd -StepName $tsStepNameRunPwsh -AddCondition $condition
```

This sample script creates the following condition on the step:

`Folder  C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\en-US exists  and  timestamp greater than "8/1/2021 16:00:00"`

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

### -FolderDateTimeOperator

When you use the **FolderTimestamp** parameter, use this parameter to specify the operator for the task sequence to evaluate the folder's timestamp.

```yaml
Type: VariableOperatorType
Parameter Sets: (All)
Aliases:
Accepted values: Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FolderPath

Specify the full path of the folder for this condition.

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

### -FolderTimestamp

To evaluate the folder's timestamp, use this parameter to specify a datetime object. To get this object, use the built-in [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) cmdlet.

Then use the **FolderDateTimeOperator** parameter to set the evaluation operator.

```yaml
Type: DateTime
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

### IResultObject#SMS_TaskSequence_FolderConditionExpression

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_FolderConditionExpression server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_folderconditionexpression-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepConditionFolder](Get-CMTSStepConditionFolder.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
