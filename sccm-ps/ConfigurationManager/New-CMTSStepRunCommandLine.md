---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/31/2021
online version:
schema: 2.0.0
---

# New-CMTSStepRunCommandLine

## SYNOPSIS

Create a **Run Command Line** step, which you can add to a task sequence.

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

This cmdlet creates a new **Run Command Line** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Run Command Line](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RunCommandLine).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first creates an object for the **Run Command Line** step. It specifies the command line and a package to use.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$step = New-CMTSStepRunCommandLine -Name "Run Command Line" -CommandLine "cmd.exe /c copy Jan98.dat c:\sales\Jan98.dat" -PackageId "XYZ00821"

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -CommandLine

Specify the command line that the task sequence runs. Include file name extensions, for example, `.exe`. Include all required settings files and command-line options.

For example: `cmd.exe /c copy Jan98.dat c:\sales\Jan98.dat`

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

By default, 64-bit operating systems use the WOW64 file system redirector to run command lines. This behavior is to properly find 32-bit versions of OS executables and libraries. Add this parameter to disable the use of the WOW64 file system redirector. Windows runs the command using native 64-bit versions of OS executables and libraries. This option has no effect when running on a 32-bit OS.

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

Specify the name of a custom task sequence variable. When you use this parameter, the step saves the last 1000 characters of the command output to the variable.

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

When you specify files or programs on the command line that don't already exist on the destination computer, use this parameter to specify the **package ID** for a package that has the necessary files. The package doesn't require a program. If the specified files exist on the destination computer, this option isn't required.

This value is a standard package ID, for example `XYZ00821`.

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

Add this parameter to run the command line as a Windows user account and not the local system account. Then use the **UserName** and **UserPassword** parameters.

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

Specify an array of integer values as exit codes from the command that the step should evaluate as success.

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

Specify an integer value that represents how long Configuration Manager allows the command line to run. This value can be from `1` minute to `999` minutes. The default value is `15` minutes.

If you enter a value that doesn't allow enough time for the specified command to complete successfully, this step fails. The entire task sequence could fail depending on step or group conditions. If the timeout expires, Configuration Manager terminates the command-line process.

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

When you use the **RunAsUser** parameter, use this parameter to specify the name of the Windows user account. To specify the account password, use the **UserPassword** parameter.

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

When you use the **RunAsUser** parameter, use this parameter to specify the password of the account that you specify with **UserName**.

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

### -WorkingDirectory

Specify the folder in which the command starts. This path can be up to 127 characters.

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

### IResultObject#SMS_TaskSequence_RunCommandLineAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_RunCommandLineAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_runcommandlineaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepRunCommandLine](Get-CMTSStepRunCommandLine.md)
[Remove-CMTSStepRunCommandLine](Remove-CMTSStepRunCommandLine.md)
[Set-CMTSStepRunCommandLine](Set-CMTSStepRunCommandLine.md)

[About task sequence steps: Run Command Line](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RunCommandLine)
