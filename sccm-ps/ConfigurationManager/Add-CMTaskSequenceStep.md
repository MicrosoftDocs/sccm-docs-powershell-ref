---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/26/2021
schema: 2.0.0
title: Add-CMTaskSequenceStep
---

# Add-CMTaskSequenceStep

## SYNOPSIS

Add a step or group to a task sequence.

## SYNTAX

### ByValue (Default)
```
Add-CMTaskSequenceStep [-InsertStepStartIndex <UInt32>] -Step <IResultObject[]> -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Add-CMTaskSequenceStep [-InsertStepStartIndex <UInt32>] -Step <IResultObject[]> -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMTaskSequenceStep [-InsertStepStartIndex <UInt32>] -Step <IResultObject[]> -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add a group or step to an existing task sequence. For more information about task sequences steps, see [Task sequence steps](/mem/configmgr/osd/understand/task-sequence-steps).

When programmatically adding steps to a task sequence, it's important to understand the index order of steps. To help visualize the index, this article uses the following example task sequence:

- step1
- step2
- step3
- step4
- group5
  - step5.1
  - step5.2
  - step5.3
  - group5.4
    - step5.4.1
  - step5.5
- step6

When you use the [task sequence editor](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_edit) to add a step, the new step is added after the currently selected step. This cmdlet works similarly, it adds the step after the specified index. You use the **InsertStepStartIndex** parameter to specify the step index.

This cmdlet can only add steps to the main level of the task sequence, not in groups. To add steps in groups, use [Set-CMTaskSequenceGroup](Set-CMTaskSequenceGroup.md). For example, with the sample task sequence, if you use **Add-CMTaskSequenceStep** with the **InsertStepStartIndex** parameter value `5`, the cmdlet adds the new step after **group5** and before **step6**.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a custom task sequence that runs two PowerShell scripts

In this example, the first two commands use the **New-CMTaskSequenceStepRunPowerShellScript** cmdlet to create step objects for the **Run Powershell Script** step. The third command creates a new custom task sequence named **Run scripts**. The fourth command passes the new task sequence object through the pipeline to **Add-CMTaskSequenceStep**, which adds the two steps.

```powershell
$step1 = New-CMTaskSequenceStepRunPowerShellScript -Name "Run script 1" -PackageID $PackageId -ScriptName "script1.ps1" -ExecutionPolicy Bypass
$step2 = New-CMTaskSequenceStepRunPowerShellScript -Name "Run script 2" -PackageID $PackageId -ScriptName "script2.ps1" -ExecutionPolicy Bypass
$ts = New-CMTaskSequence -Name "Run scripts" -CustomTaskSequence
$ts | Add-CMTaskSequenceStep -Step ($step1, $step2)
```

The resulting task sequence looks like the following list:

- Run script 1
- Run script 2

The steps are ordered this way because of how they're ordered in the **Step** parameter.

### Example 2: Create a custom task sequence that runs two PowerShell scripts with a different order

This example is similar to Example 1, except it uses two instances of the **Add-CMTaskSequenceStep** cmdlet.

```powershell
$step1 = New-CMTaskSequenceStepRunPowerShellScript -Name "Run script 1" -PackageID $PackageId -ScriptName "script1.ps1" -ExecutionPolicy Bypass
$step2 = New-CMTaskSequenceStepRunPowerShellScript -Name "Run script 2" -PackageID $PackageId -ScriptName "script2.ps1" -ExecutionPolicy Bypass
$ts = New-CMTaskSequence -Name "Run scripts" -CustomTaskSequence
$ts | Add-CMTaskSequenceStep -Step $step1
$ts | Add-CMTaskSequenceStep -Step $step2
```

The resulting task sequence looks like the following list:

- Run script 2
- Run script 1

Because of how each instance of **Add-CMTaskSequenceStep** is ordered, and neither uses the **InsertStepStartIndex** parameter, by default they use index `0`. So the cmdlet adds the second step _before_ the first step.

### Example 3: Add a step at a specific index

This example first uses the **New-CMTSStepSetVariable** cmdlet to create a step object for the **Set Task Sequence Variable** step. It then adds this step to the task sequence named **ts1** after the step at index **2**. Using the example task sequence in the [Description](#description), this command adds **newStep** in between **step2** and **step3**.

```powershell
$step = New-CMTSStepSetVariable -name "newStep" -TaskSequenceVariable "testVar" -TaskSequenceVariableValue "testValue"
Add-CMTaskSequenceStep -TaskSequenceName "ts1" -Step $step -InsertStepStartIndex 2
```

### Example 4: Copy a task sequence and add a new step

This example copies an existing task sequence, and then renames it. The next set of steps reconfigures the security scope. It then gets the ID for a package, and copies a condition object from another step. In the last group, it creates a new **Run Command Line** step that uses the package and condition objects. It then adds the new step to the new task sequence at index 11.

```powershell
$ts = Copy-CMTaskSequence -Name "Deploy Windows 10 (v1)"
$ts | Set-CMTaskSequence -NewName "Deploy Windows 10 (v2)"

$ts | Add-CMObjectSecurityScope -Name "Contoso main" | Out-Null
$ts | Remove-CMObjectSecurityScope -Name "Default" -Force |Out-Null

$pkgId = (Get-CMPackage -Name "Widget tool" -Fast).PackageID
$condition = ($ts | Get-CMTaskSequenceStep -StepName "Restart in Windows PE").Condition.Operands

$step = New-CMTaskSequenceStepRunCommandLine -CommandLine "widget.exe /q" -PackageId $pkgId -Name "Install Widget in Windows PE" -Condition $condition
$ts | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
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

Specify a task sequence object to which the cmdlet adds the step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md), [Copy-CMTaskSequence](Copy-CMTaskSequence.md), or [New-CMTaskSequence](New-CMTaskSequence.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InsertStepStartIndex

Specify an integer value for the task sequence index. The cmdlet adds the new step after this specified index. For example, using the example task sequence in the [Description](#description), if you specify a value of `4`, the cmdlet adds the new step after **step4**.

If you specify a value of `0`, the cmdlet adds the new step at the top of the task sequence. This behavior is the default if you don't specify this parameter. For example, the cmdlet adds the new step _before_ **step1**.

There's no maximum value. If you specify a value that's greater than the last step's index, the cmdlet adds the new step at the end of the task sequence. For example, if you specify a value of `10`, the cmdlet adds the new step after **step6**.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: InsertStepsStartIndex

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Step

Specify one or more step objects to add to the task sequence. To get this object, use one of the **New-CMTSStep\*** cmdlets. For example, [Get-CMTSStepApplyDataImage](Get-CMTSStepApplyDataImage.md).

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Steps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceId

Specify the ID of a task sequence to which the cmdlet adds the step. This ID is the task sequence package ID, for example `XYZ00861`.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id, TaskSequencePackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify the name of a task sequence to which the cmdlet adds the step.

```yaml
Type: String
Parameter Sets: ByName
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

While not listed in the related links section, you can use the **Get-CMTSStep\***, **New-CMTSStep\***, **Remove-CMTSStep\***, and **Set-CMTSStep\*** cmdlets. For example:

- [Get-CMTSStepApplyDataImage](Get-CMTSStepApplyDataImage.md)
- [New-CMTSStepApplyDataImage](New-CMTSStepApplyDataImage.md)
- [Remove-CMTSStepApplyDataImage](Remove-CMTSStepApplyDataImage.md)
- [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md)

There's a set of these cmdlets for each task sequence step.

## RELATED LINKS

[Get-CMTaskSequenceStep](Get-CMTaskSequenceStep.md)
[Get-CMTaskSequenceStepCondition](Get-CMTaskSequenceStepCondition.md)
[Remove-CMTaskSequenceStep](Remove-CMTaskSequenceStep.md)

[Get-CMTaskSequenceGroup](Get-CMTaskSequenceGroup.md)
[New-CMTaskSequenceGroup](New-CMTaskSequenceGroup.md)
[Set-CMTaskSequenceGroup](Set-CMTaskSequenceGroup.md)

[About task sequence steps](/mem/configmgr/osd/understand/task-sequence-steps)
