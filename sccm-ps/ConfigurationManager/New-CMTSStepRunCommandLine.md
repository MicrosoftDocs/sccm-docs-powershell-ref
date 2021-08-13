---
description: Creates a t s step run command line.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMTSStepRunCommandLine
---

# New-CMTSStepRunCommandLine

## SYNOPSIS

Creates a t s step run command line.

## SYNTAX

### ByName (Default)
```
New-CMTSStepRunCommandLine -CommandLine <String> [-DisableWow64Redirection] [-PackageId <String>] [-RunAsUser]
 [-SuccessCode <Int32[]>] [-Timeout <Int32>] [-UserName <String>] [-UserPassword <SecureString>]
 [-WorkingDirectory <String>] [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>]
 [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RunScriptFromSource
```
New-CMTSStepRunCommandLine -CommandLine <String> [-DisableWow64Redirection] [-OutputVariableName <String>]
 [-PackageId <String>] [-RunAsUser] [-SuccessCode <Int32[]>] [-Timeout <Int32>] [-UserName <String>]
 [-UserPassword <SecureString>] [-WorkingDirectory <String>] [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RunScriptFromPackage
```
New-CMTSStepRunCommandLine -CommandLine <String> [-DisableWow64Redirection] [-OutputVariableName <String>]
 [-PackageId <String>] [-RunAsUser] [-SuccessCode <Int32[]>] [-Timeout <Int32>] [-UserName <String>]
 [-UserPassword <SecureString>] [-WorkingDirectory <String>] [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -CommandLine
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

### -DisableWow64Redirection
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableRedirectionFor64BitFileSystem

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
Parameter Sets: ByName
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputVariableName
Use this parameter to configure the following setting in the **Run Command Line** task sequence step: **Output to task sequence variable**. Save the command output to a custom task sequence variable.

```yaml
Type: String
Parameter Sets: RunScriptFromSource, RunScriptFromPackage
Aliases: Output, OutputVariable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageId
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

### -RunAsUser
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

### -SuccessCode
```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: SuccessCodes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Timeout
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
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

### -UserPassword
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

### -WorkingDirectory
```yaml
Type: String
Parameter Sets: (All)
Aliases: StartIn

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

### IResultObject#SMS_TaskSequence_RunCommandLineAction
## NOTES

## RELATED LINKS
