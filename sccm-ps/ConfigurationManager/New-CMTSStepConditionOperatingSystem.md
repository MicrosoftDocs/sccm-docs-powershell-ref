---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionOperatingSystem

## SYNOPSIS

Create an _OS version_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionOperatingSystem -SupportedPlatform <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an _OS version_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMSupportedPlatform** cmdlet to create a supported platform object that includes Windows 10 and Windows 11 64-bit clients. Next, it uses that object to create the task sequence step condition object.

It then uses the **Set-CMTSStepSetDynamicVariable** cmdlet to add this condition object to the **Set Dynamic Variables** step of the **Default OS deployment** task sequence.

```powershell
$osPlat = Get-CMSupportedPlatform -Name "*Windows 1? (64-bit) Client" -Fast

$condition = New-CMTSStepConditionOperatingSystem -SupportedPlatform $osPlat

$tsNameOsd = "Default OS deployment"
$tsStepNameDynVar = "Set Dynamic Variables"

Set-CMTSStepSetDynamicVariable -TaskSequenceName $tsNameOsd -StepName $tsStepNameDynVar -AddCondition $condition
```

This sample script creates the following condition on the step:

`Operating System  equals All Windows 10 (64-bit) Or All Windows 11 (64-bit)`

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

### -SupportedPlatform

Specify one or more supported platform objects for this condition. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SupportedPlatforms

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

### IResultObject#SMS_TaskSequence_OSConditionGroup

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_OSConditionGroup server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_osconditiongroup-server-wmi-class).

To create an OS language condition, use the [New-CMTSStepConditionOperatingSystemLanguage](New-CMTSStepConditionOperatingSystemLanguage.md) cmdlet.

## RELATED LINKS

[Get-CMTSStepConditionOperatingSystem](Get-CMTSStepConditionOperatingSystem.md)

[New-CMTSStepConditionOperatingSystemLanguage](New-CMTSStepConditionOperatingSystemLanguage.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
