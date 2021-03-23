---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMTSStepRunTaskSequence

## SYNOPSIS

Use this cmdlet to create the task sequence step **Run Task Sequence**.

## SYNTAX

```
New-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1906, se this cmdlet to create the task sequence step **Run Task Sequence**.

## EXAMPLES

### Example 1: Create the task sequence step

```powershell
$refSubTaskSequence = Get-CMTaskSequence -Name "Child task sequence"
$myStep = New-CMTSStepRunTaskSequence -Name "Run child task sequence" -RunTaskSequence $refSubTaskSequence
```

## PARAMETERS

### -Condition

Specify a task sequence step condition object. For example, use the [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md) cmdlet.

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

This parameter is the same as the following setting on the **Options** tab of the **Run Task Sequence** step in the **Task Sequence Editor** in the console: **Continue on error**.

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

Specify a description for the task sequence step.

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

This parameter is the same as the following setting on the **Options** tab of the **Run Task Sequence** step in the **Task Sequence Editor** in the console: **Disable this step**.

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

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

Specify a name for the task sequence step.

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

### -RunTaskSequence

Specify an object for the task sequence that you want this step to run. This parameter is the same as the following setting on the **Properties** tab of the **Run Task Sequence** step in the **Task Sequence Editor** in the console: **Select task sequence to run**.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: Child

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

### IResultObject#SMS_TaskSequence_SubTasksequence

## NOTES

## RELATED LINKS
