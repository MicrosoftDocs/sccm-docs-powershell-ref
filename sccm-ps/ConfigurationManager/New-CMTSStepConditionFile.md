---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionFile

## SYNOPSIS

Create a _file properties_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionFile [-FileDateTimeOperator <VariableOperatorType>] -FilePath <String>
 [-FileTimestamp <DateTime>] [-FileVersion <String>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a _file properties_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

There are three types of checks that you can do with this condition:

- To check if the file exists, use the required **FilePath** parameter.
- To also check the file version, use the **FileVersion** and **VersionOperator** parameters.
- To also check the file timestamp, use the **FileTimestamp** and **FileDateTimeOperator** parameters.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example checks for the existence and timestamp for one of the Configuration Manager PowerShell module help files. It creates a file condition object for the file and that its timestamp is greater than August 2, 2021.

It then uses the **Set-CMTSStepRunPowerShellScript** cmdlet to add this condition object to the **Run PowerShell Script** step of the **Default OS deployment** task sequence.

```powershell
$file = "C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\en-US\AdminUI.PS.dll-Help.xml"
$datetime = Get-Date ("August 2, 2021")

$condition = New-CMTSStepConditionFile -FilePath $file -FileTimestamp $datetime -FileDateTimeOperator Greater

$tsNameOsd = "Default OS deployment"
$tsStepNameRunPwsh = "Run PowerShell Script"

Set-CMTSStepRunPowerShellScript -TaskSequenceName $tsNameOsd -StepName $tsStepNameRunPwsh -AddCondition $condition
```

This sample script creates the following condition on the step:

`File  C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\en-US\AdminUI.PS.dll-Help.xml exists  and  timestamp greater than "8/1/2021 16:00:00"`

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

### -FileDateTimeOperator

When you use the **FileTimestamp** parameter, use this parameter to specify the operator for the task sequence to evaluate the file's timestamp.

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

### -FilePath

Specify the full path including the name of the file for this condition.

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

### -FileTimestamp

To evaluate the file's timestamp, use this parameter to specify a datetime object. To get this object, use the built-in [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) cmdlet.

Then use the **FileDateTimeOperator** parameter to set the evaluation operator.

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

### -FileVersion

To evaluate the file's version, use this parameter to specify the version string.

Then use the **VersionOperator** parameter to set the evaluation operator.

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

### -VersionOperator

When you use the **FileVersion** parameter, use this parameter to specify the operator for the task sequence to evaluate the file's version.

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

### IResultObject#SMS_TaskSequence_FileConditionExpression

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_FileConditionExpression server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_fileconditionexpression-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepConditionFile](Get-CMTSStepConditionFile.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
