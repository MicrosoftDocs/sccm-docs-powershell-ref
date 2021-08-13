---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/12/2021
schema: 2.0.0
title: New-CMTSStepInstallApplication
---

# New-CMTSStepInstallApplication

## SYNOPSIS

Create an **Install Application** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepInstallApplication [-Application <IResultObject[]>] [-BaseVariableName <String>]
 [-ClearCache <Boolean>] [-ContinueOnInstallError] [-RetryCount <Int32>] [-Condition <IResultObject[]>]
 [-ContinueOnError] [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Install Application** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Install Application](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_InstallApplication).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets an app object for the **Central app** and saves it in the **$app** variable.

The next line creates an object for the **Install Application** step, using the **$app** variable.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$app = Get-CMApplication -Name "Central app"

$step = New-CMTSStepInstallApplication -Name "Install Application" -Application $app

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -Application

Specify one or more application objects to install. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Applications

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BaseVariableName

Use this parameter to install applications according to a dynamic variable list. Then the task sequence installs applications using this base variable name. For more information, see [Install applications according to dynamic variable list](/mem/configmgr/osd/understand/task-sequence-steps#install-applications-according-to-dynamic-variable-list).

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

### -ClearCache

Set this parameter to `$true` to clear application content from the client cache after installing the app. This behavior is beneficial on devices with small hard drives or when installing lots of large apps in succession.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RemoveFromCache

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

Add this parameter to continue installing other applications in the list if an application fails to install. If you don't specify this setting, and the installation fails, the step immediately ends.

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

### -RetryCount

If one of the application installations unexpectedly restarts the computer, retry this step for the number of times that you specify with this parameter. By default, the step retries twice. Specify an integer value from `1` to `5`.

```yaml
Type: Int32
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

### IResultObject#SMS_TaskSequence_InstallApplicationAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_InstallApplicationAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_installapplicationaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepInstallApplication](Get-CMTSStepInstallApplication.md)
[Remove-CMTSStepInstallApplication](Remove-CMTSStepInstallApplication.md)
[Set-CMTSStepInstallApplication](Set-CMTSStepInstallApplication.md)

[About task sequence steps: Install Application](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_InstallApplication)
