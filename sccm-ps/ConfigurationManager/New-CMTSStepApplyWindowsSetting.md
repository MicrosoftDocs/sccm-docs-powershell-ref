---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/11/2021
online version:
schema: 2.0.0
---

# New-CMTSStepApplyWindowsSetting

## SYNOPSIS

Create an **Apply Windows Settings** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepApplyWindowsSetting [-InputLocale <String>] -OrganizationName <String> [-Password <SecureString>]
 [-ProductKey <String>] [-SystemLocale <String>] [-TimeZone <TimeZoneInfo>] [-UILanguage <String>]
 [-UILanguageFallback <String>] [-UserLocale <String>] -UserName <String> [-Condition <IResultObject[]>]
 [-ContinueOnError] [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Apply Windows Settings** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Apply Windows Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyWindowsSettings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets a time zone object.
The next line creates an object for the **Apply Windows Settings** step that specifies various location-specific settings.
It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$tz = Get-TimeZone -Id "Russian Standard Time"

$step = New-CMTSStepApplyWindowsSetting -Name "Apply Windows Settings for Moscow office" -UserName "Natalia Ivanovna" -OrganizationName "Contoso" -TimeZone $tz -InputLocale "ru-ru" -SystemLocale "ru-ru" -UILanguage "ru-ru" UserLocale "ru-ru"

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

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

### -InputLocale

Use this parameter to set the locale setting for the default keyboard layout. For example, to set it to Russian (Russia), specify the string **ru-ru**: `-InputLocale "ru-ru"`

For more information on these Windows setup answer file values, see [Microsoft-Windows-International-Core](/windows-hardware/customize/desktop/unattend/microsoft-windows-international-core).

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

### -OrganizationName

Specify the registered organization name to associate with the destination computer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RegisteredOrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Password

To enable the local **Administrator** account, use this parameter to specify its password. If you don't include this parameter, the local account is disabled by default with a randomly generated password.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductKey

Specify the product key to use for the Windows installation on the destination computer.

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

### -SystemLocale

Use this parameter to set the language for non-Unicode programs. For example, to set it to Russian (Russia), specify the string **ru-ru**: `-SystemLocale "ru-ru"`

For more information on these Windows setup answer file values, see [Microsoft-Windows-International-Core](/windows-hardware/customize/desktop/unattend/microsoft-windows-international-core).

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

### -TimeZone

Specify the time zone to configure on the destination computer. To get this object, use the [Get-TimeZone](/powershell/module/microsoft.powershell.management/get-timezone) built-in cmdlet.

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UILanguage

Use this parameter to set the system default user interface (UI) language. For example, to set it to Russian (Russia), specify the string **ru-ru**: `-UILanguage "ru-ru"`

For more information on these Windows setup answer file values, see [Microsoft-Windows-International-Core](/windows-hardware/customize/desktop/unattend/microsoft-windows-international-core).

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

### -UILanguageFallback

Use this parameter to set the fallback language if the system default UI language is only partially localized. For example, to set it to Russian (Russia), specify the string **ru-ru**: `-UILanguageFallback "ru-ru"`

For more information on these Windows setup answer file values, see [Microsoft-Windows-International-Core](/windows-hardware/customize/desktop/unattend/microsoft-windows-international-core).

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

### -UserLocale

Use this parameter to set the per-user settings used for formatting dates, times, currency, and numbers. For example, to set it to Russian (Russia), specify the string **ru-ru**: `-UserLocale "ru-ru"`

For more information on these Windows setup answer file values, see [Microsoft-Windows-International-Core](/windows-hardware/customize/desktop/unattend/microsoft-windows-international-core).

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

### -UserName

Specify the registered user name to associate with the destination computer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RegisteredUserName

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

### IResultObject#SMS_TaskSequence_ApplyWindowsSettingsAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_ApplyWindowsSettingsAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_applywindowssettingsaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepApplyWindowsSetting](Get-CMTSStepApplyWindowsSetting.md)
[Remove-CMTSStepApplyWindowsSetting](Remove-CMTSStepApplyWindowsSetting.md)
[Set-CMTSStepApplyWindowsSetting](Set-CMTSStepApplyWindowsSetting.md)

[About task sequence steps: Apply Windows Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyWindowsSettings)
