---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/11/2021
online version:
schema: 2.0.0
---

# New-CMTSStepAutoApplyDriver

## SYNOPSIS

Create an **Auto Apply Drivers** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepAutoApplyDriver [-AllowUnsignedDriver] [-DriverCategory <IResultObject[]>]
 [-InstallDriverOption <InstallDriverType>] [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Auto Apply Drivers** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Auto Apply Drivers](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_AutoApplyDrivers).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMCategory** cmdlet to get the category of Surface drivers.
The next line creates an object for the **Auto Apply Drivers** step that installs all compatible drivers from those in the Surface drivers category.
It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$category = Get-CMCategory -CategoryType DriverCategories -Name "Surface"

$step = New-CMTSStepAutoApplyDriver -Name "Auto Apply Drivers" -DriverCategory $category -InstallDriverOption InstallAllCompatible

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -AllowUnsignedDriver

Add this parameter to allow Windows to install drivers without a digital signature.

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

### -DriverCategory

Specify one or more driver category objects, to limit driver matching to only consider drivers in the selected categories. To get this object, use the [Get-CMCategory](Get-CMCategory.md) cmdlet with `-CategoryType DriverCategories`.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DriverCategories

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

### -InstallDriverOption

Specify how this step behaves:

- `BestMatch`: Install only the best matched compatible drivers.
- `InstallAllCompatible`: Installs all drivers compatible for each detected hardware device.

```yaml
Type: InstallDriverType
Parameter Sets: (All)
Aliases:
Accepted values: BestMatch, InstallAllCompatible

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

### IResultObject#SMS_TaskSequence_AutoApplyAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_AutoApplyAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_autoapplyaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepAutoApplyDriver](Get-CMTSStepAutoApplyDriver.md)
[Remove-CMTSStepAutoApplyDriver](Remove-CMTSStepAutoApplyDriver.md)
[Set-CMTSStepAutoApplyDriver](Set-CMTSStepAutoApplyDriver.md)

[About task sequence steps: Auto Apply Drivers](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_AutoApplyDrivers)
