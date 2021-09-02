---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionOperatingSystemLanguage

## SYNOPSIS

Create an _OS language_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionOperatingSystemLanguage -OSLanguageId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an _OS language_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first creates an OS language condition object for the **Irish (Ireland)** language.

It then uses the **Set-CMTSStepSetDynamicVariable** cmdlet to add this condition object to the **Set Dynamic Variables** step of the **Default OS deployment** task sequence.

```powershell
$langIdIrish = 2108
$condition = New-CMTSStepConditionOperatingSystemLanguage -OSLanguageId $langIdIrish

$tsNameOsd = "AAron"
$tsStepNameDynVar = "Set Dynamic Variables"

Set-CMTSStepSetDynamicVariable -TaskSequenceName $tsNameOsd -StepName $tsStepNameDynVar -AddCondition $condition
```

This sample script creates the following condition on the step:

`WMI Query  SELECT OsLanguage FROM Win32_OperatingSystem WHERE OsLanguage='2108'`

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

### -OSLanguageId

Use this parameter to configure the specific OS language. This check compares the language ID to the **OSLanguage** property of the **Win32_OperatingSystem** WMI class on the client. For example, `1033` for **English (United States)**.

This value is the decimal equivalent of the Windows _language ID_. For example, `1033` is `0x0409` for **English (United States)**, and `2070` is `0x0816` for **Portuguese (Portugal)**. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

```yaml
Type: Int32
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

### IResultObject#SMS_TaskSequence_WMIConditionExpression

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_WMIConditionExpression server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_wmiconditionexpression-server-wmi-class).

You can only set a single language ID per condition. To add a condition for multiple language IDs, first create multiple OS language conditions. Then nest them in an _if statement_ condition with the [New-CMTSStepConditionIfStatement](New-CMTSStepConditionIfStatement.md) cmdlet.

To get an OS language condition, use the [Get-CMTSStepConditionQueryWmi](Get-CMTSStepConditionQueryWmi.md) cmdlet. The task sequence editor option to add an **OS Language** condition is a shortcut for a specific WMI query.

## RELATED LINKS

[Get-CMTSStepConditionQueryWmi](Get-CMTSStepConditionQueryWmi.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
