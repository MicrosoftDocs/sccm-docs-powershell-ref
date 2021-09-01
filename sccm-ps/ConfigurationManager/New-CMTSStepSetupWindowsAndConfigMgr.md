---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/01/2021
online version:
schema: 2.0.0
---

# New-CMTSStepSetupWindowsAndConfigMgr

## SYNOPSIS

Create a **Setup Windows and ConfigMgr** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepSetupWindowsAndConfigMgr [-InstallationProperty <String>] -PackageId <String>
 [-PreproductionPackageId <String>] [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>]
 [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Setup Windows and ConfigMgr** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Setup Windows and ConfigMgr](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetupWindowsandConfigMgr).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first creates an object for the **Setup Windows and ConfigMgr** step, using the package with ID **XYZ0002**.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$step = New-CMTSStepSetupWindowsAndConfigMgr -Name "Setup Windows and ConfigMgr" -PackageId "XYZ0002"

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

Add this parameter to enable the step option **Continue on error**.

Specifically with this step, if there's an error, the task sequence fails whether or not this setting is enabled.

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

### -InstallationProperty

The task sequence step automatically specifies site assignment and the default configuration. Use this parameter to specify any additional installation properties to use when you install the client. To enter multiple installation properties, separate them with a space.

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstallationProperties

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

Specify the **package ID** of the the Configuration Manager client installation package to use with this step. This value is a standard package ID, for example `XYZ0002`.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClientPackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreproductionPackageId

Specify the **package ID** of the pre-production client installation package to use with this step.

If there's a pre-production client package available, and the computer is a member of the piloting collection, the task sequence uses this package instead of the production client package. The pre-production client is a newer version for testing in the production environment.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PreproductionClientPackageId

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

### IResultObject#SMS_TaskSequence_SetupWindowsAndSMSAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_SetupWindowsAndSMSAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_setupwindowsandsmsaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepSetupWindowsAndConfigMgr](Get-CMTSStepSetupWindowsAndConfigMgr.md)
[Remove-CMTSStepSetupWindowsAndConfigMgr](Remove-CMTSStepSetupWindowsAndConfigMgr.md)
[Set-CMTSStepSetupWindowsAndConfigMgr](Set-CMTSStepSetupWindowsAndConfigMgr.md)

[About task sequence steps: Setup Windows and ConfigMgr](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetupWindowsandConfigMgr)
