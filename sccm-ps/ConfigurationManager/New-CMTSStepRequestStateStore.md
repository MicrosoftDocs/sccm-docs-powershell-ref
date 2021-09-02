---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2021
online version:
schema: 2.0.0
---

# New-CMTSStepRequestStateStore

## SYNOPSIS

Create the **Request State Store** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepRequestStateStore [-FallbackToAccount <Boolean>] [-RequestOption <RequestType>]
 [-RetryCount <Int32>] [-RetryTime <Int32>] [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Request State Store** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Request State Store](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RequestStateStore).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example creates an object for the **Request State Store** step to capture user state and specifies typical settings.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$step = New-CMTSStepRequestStateStore -Name "Request State Store" -RequestOption Capture -FallbackToAccount $false -RetryCount 3 -RetryTime 60

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

### -FallbackToAccount

When you set this value to `$true`, if the task sequence can't access the state migration point using the computer account, it uses the network access account credentials to connect. This option is less secure because other computers could use the network access account to access the stored state. This option might be necessary if the destination computer isn't domain joined.

For more information, see [Network access account](/mem/configmgr/core/plan-design/hierarchy/accounts#network-access-account).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: FallbackToNaa

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

### -RequestOption

Specify the reason to request access to the state migration point:

- `Capture`: Capture state from the computer. If the Configuration Manager site has multiple active state migration points, this step finds a state migration point with available disk space. The task sequence queries the management point for a list of state migration points, and then evaluates each until it finds one that meets the minimum requirements.

- `Restore`: Restore state from another computer. If there are multiple state migration points, this step finds the state migration point that has the state for the destination computer.

```yaml
Type: RequestType
Parameter Sets: (All)
Aliases:
Accepted values: Capture, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetryCount

Specify the number of times that this step tries to find an appropriate state migration point before failing.

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

### -RetryTime

Specify the amount of time in seconds that the task sequence step waits between retry attempts.

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

### IResultObject#SMS_TaskSequence_RequestStateStoreAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_RequestStateStoreAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_requeststatestoreaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepRequestStateStore](Get-CMTSStepRequestStateStore.md)
[Remove-CMTSStepRequestStateStore](Remove-CMTSStepRequestStateStore.md)
[Set-CMTSStepRequestStateStore](Set-CMTSStepRequestStateStore.md)

[About task sequence steps: Request State Store](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RequestStateStore)
