---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
online version:
schema: 2.0.0
---

# New-CMTSStepApplyDriverPackage

## SYNOPSIS

Create an **Apply Driver Package** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepApplyDriverPackage [-BootCriticalContentUniqueId <String>] [-BootCriticalDriverId <String>]
 [-BootCriticalHardwareComponent <String>] [-BootCriticalId <String>] [-BootCriticalInfFile <String>]
 [-EnableRecurse] [-EnableUnsignedDriver] -PackageId <String> [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Apply Driver Package** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Apply Driver Package](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyDriverPackage).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMDriverPackage** cmdlet to get an object for the package of **Surface 4 drivers**. It saves this object in the **$pkgDriver** variable. The next step creates an object for the **Apply Driver Package** step, getting the ID from the **$pkgDriver** object.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$pkgDriver = Get-CMDriverPackage -Name "Surface 4 drivers" -Fast
$step = New-CMTSStepApplyDriverPackage -Name "Apply driver package" -PackageId $pkgDriver.PackageID

$tsName = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsName -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -BootCriticalContentUniqueId

This parameter is deprecated, it only applies to pre-Windows Vista OS versions.

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

### -BootCriticalDriverId

This parameter is deprecated, it only applies to pre-Windows Vista OS versions.

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

### -BootCriticalHardwareComponent

This parameter is deprecated, it only applies to pre-Windows Vista OS versions.

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

### -BootCriticalId

This parameter is deprecated, it only applies to pre-Windows Vista OS versions.

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

### -BootCriticalInfFile

This parameter is deprecated, it only applies to pre-Windows Vista OS versions.

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

Specify a condition object to use with this step.

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

### -EnableRecurse

Add this parameter to install the driver package by running DISM with the recurse option.

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

### -EnableUnsignedDriver

Add this parameter to do an unattended installation of unsigned drivers on a version of Windows where this action is allowed.

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

### -PackageId

Specify the **package ID** of the driver package for this step to apply. This value is a standard package ID, for example, `XYZ0030D`.

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

### IResultObject#SMS_TaskSequence_ApplyDriverPackageAction

## NOTES

## RELATED LINKS

[Get-CMTSStepApplyDriverPackage](Get-CMTSStepApplyDriverPackage.md)
[Remove-CMTSStepApplyDriverPackage](Remove-CMTSStepApplyDriverPackage.md)
[Set-CMTSStepApplyDriverPackage](Set-CMTSStepApplyDriverPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[About task sequence steps: Apply Driver Package](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyDriverPackage)
