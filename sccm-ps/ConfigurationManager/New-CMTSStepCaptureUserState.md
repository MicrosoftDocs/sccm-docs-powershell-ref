---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/12/2021
online version:
schema: 2.0.0
---

# New-CMTSStepCaptureUserState

## SYNOPSIS

Create an **Capture User State** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepCaptureUserState [-ConfigFile <String[]>] [-ContinueOnLockedFile <Boolean>]
 [-FileAccessOption <FileAccessType>] [-ModeOption <ModeType>] [-OfflineUserState <Boolean>]
 -Package <IResultObject> [-SkipEncryptedFile <Boolean>] [-UseHardLinks <Boolean>] [-VerboseLogging <Boolean>]
 [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>] [-Disable] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Capture User State** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets a package object for the User State Migration Tool (USMT).
The next line creates an object for the **Capture User State** step, which uses that USMT package and configures several step settings.
It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$pkgUsmt = Get-CMPackage -Name "User State Migration Tool for Windows" -Fast

$step = New-CMTSStepCaptureUserState -Name "Capture User State" -Package $pkgUsmt -ModeOption Standard -VerboseLogging $true -FileAccessOption Normal -ContinueOnLockedFile $true -UseHardLinks $true

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

### -ConfigFile

When you specify `-ModeOption Customize` to customize how user profiles are captured, use this parameter to specify the file names of custom XML configuration files. These files need to be in the USMT package.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ConfigFiles

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

### -ContinueOnLockedFile

When you specify `-FileAccessOption Normal`, set this parameter to `$true` to allow USMT to continue if some files can't be captured.

```yaml
Type: Boolean
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

### -FileAccessOption

There are two options for how USMT accesses the file system:

- `Normal`: USMT uses standard file system access. When you specify this option, you can also enable **ContinueOnLockedFile**, **OfflineUserState**, and **-**.

- `VolumeCopyShadowService`: USMT uses the Volume Copy Shadow Services (VSS).

```yaml
Type: FileAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Normal, VolumeCopyShadowService

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

### -ModeOption

There are two modes in which USMT can operate:

- `Standard`: Capture all user profiles by using standard options. This option is the default.

- `Customize`: Customize how user profiles are captured. If you specify this option, use the **ConfigFile** parameter to specify the custom XML configuration files.

```yaml
Type: ModeType
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Customize

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

### -OfflineUserState

When you specify `-FileAccessOption Normal`, set this parameter to `$true` to capture in offline mode in Windows PE.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package

Specify an object for the USMT package. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: UserStateMigrationToolPackage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipEncryptedFile

Set this parameter to `$true` to skip files that use the encrypting file system (EFS).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseHardLinks

When you specify `-FileAccessOption Normal`, set this parameter to `$true` to capture locally by using NTFS hard-links.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VerboseLogging

Set this parameter to `$true` to enable USMT verbose logging.

```yaml
Type: Boolean
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

### IResultObject#SMS_TaskSequence_CaptureUserStateAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_CaptureUserStateAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_captureuserstateaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepCaptureUserState](Get-CMTSStepCaptureUserState.md)
[Remove-CMTSStepCaptureUserState](Remove-CMTSStepCaptureUserState.md)
[Set-CMTSStepCaptureUserState](Set-CMTSStepCaptureUserState.md)

[About task sequence steps: Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState)
