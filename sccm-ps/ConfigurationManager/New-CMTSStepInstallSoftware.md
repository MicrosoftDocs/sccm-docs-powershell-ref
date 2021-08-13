---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2021
schema: 2.0.0
title: New-CMTSStepInstallSoftware
---

# New-CMTSStepInstallSoftware

## SYNOPSIS

Create an **Install Package** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepInstallSoftware [-BaseVariableName <String>] [-ContinueOnInstallError] [-Program <IResultObject>]
 [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>] [-Disable] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Install Package** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Install Package](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_InstallPackage).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMProgram** cmdlet to get the **Install** program from the package with ID **XYZ0000F**.

The next line creates an object for the **Install Package** step, using the program variable.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$program = Get-CMProgram -PackageId "XYZ0000F" -ProgramName "Install"

$step = New-CMTSStepInstallSoftware -Name "Install Package" -Program $program

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -BaseVariableName

Use this parameter to install software packages according to a dynamic variable list. Then the task sequence installs packages using this base variable name. For more information, see [Install software packages according to dynamic variable list](/mem/configmgr/osd/understand/task-sequence-steps#install-software-packages-according-to-dynamic-variable-list).

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

### -ContinueOnInstallError

Add this parameter to continue installing other packages in the list if a package fails to install. If you don't specify this setting, and the installation fails, the step immediately ends.

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

### -Program

Specify a program object from a package to install. To get this object, use the [Get-CMProgram](Get-CMProgram.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

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

### IResultObject#SMS_TaskSequence_InstallSoftwareAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_InstallSoftwareAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_installsoftwareaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepInstallSoftware](Get-CMTSStepInstallSoftware.md)
[Remove-CMTSStepInstallSoftware](Remove-CMTSStepInstallSoftware.md)
[Set-CMTSStepInstallSoftware](Set-CMTSStepInstallSoftware.md)

[About task sequence steps: Install Package](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_InstallPackage)
