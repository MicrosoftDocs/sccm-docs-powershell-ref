---
author: aczechowski
description: Creates a t s step run power shell script.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMTSStepRunPowerShellScript
titleSuffix: Configuration Manager
---

# New-CMTSStepRunPowerShellScript

## SYNOPSIS

Creates a t s step run power shell script.

## SYNTAX

### ByName (Default)
```
New-CMTSStepRunPowerShellScript -Name <String> [-SuccessCode <Int32[]>] [-Description <String>]
 [-ContinueOnError] [-Disable] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RunScriptFromSource
```
New-CMTSStepRunPowerShellScript -Name <String> -SourceScript <String> [-WorkingDirectory <String>]
 [-TimeoutMins <Int32>] [-UserName <String>] [-UserPassword <SecureString>] [-OutputVariableName <String>]
 [-Parameter <String>] [-SuccessCode <Int32[]>] [-ExecutionPolicy <ExecutionPolicyType>]
 [-Description <String>] [-ContinueOnError] [-Disable] [-Condition <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RunScriptFromPackage
```
New-CMTSStepRunPowerShellScript -Name <String> -PackageId <String> -ScriptName <String>
 [-WorkingDirectory <String>] [-TimeoutMins <Int32>] [-UserName <String>] [-UserPassword <SecureString>]
 [-OutputVariableName <String>] [-Parameter <String>] [-SuccessCode <Int32[]>]
 [-ExecutionPolicy <ExecutionPolicyType>] [-Description <String>] [-ContinueOnError] [-Disable]
 [-Condition <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -Condition
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
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -ExecutionPolicy
```yaml
Type: ExecutionPolicyType
Parameter Sets: RunScriptFromSource, RunScriptFromPackage
Aliases: PowerShellExecutionPolicy
Accepted values: AllSigned, Undefined, Bypass

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -OutputVariableName
{{ Fill OutputVariableName Description }}

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
Parameter Sets: RunScriptFromPackage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Parameter
```yaml
Type: String
Parameter Sets: RunScriptFromSource, RunScriptFromPackage
Aliases: Parameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptName
```yaml
Type: String
Parameter Sets: RunScriptFromPackage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceScript
{{ Fill SourceScript Description }}

```yaml
Type: String
Parameter Sets: RunScriptFromSource
Aliases: SourceCode

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuccessCode
{{ Fill SuccessCode Description }}

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

### -TimeoutMins
{{ Fill TimeoutMins Description }}

```yaml
Type: Int32
Parameter Sets: RunScriptFromSource, RunScriptFromPackage
Aliases: TimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
{{ Fill UserName Description }}

```yaml
Type: String
Parameter Sets: RunScriptFromSource, RunScriptFromPackage
Aliases: User

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPassword
{{ Fill UserPassword Description }}

```yaml
Type: SecureString
Parameter Sets: RunScriptFromSource, RunScriptFromPackage
Aliases: Password

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
{{ Fill WorkingDirectory Description }}

```yaml
Type: String
Parameter Sets: RunScriptFromSource, RunScriptFromPackage
Aliases: StartIn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_RunPowerShellScriptAction

## NOTES

## RELATED LINKS
