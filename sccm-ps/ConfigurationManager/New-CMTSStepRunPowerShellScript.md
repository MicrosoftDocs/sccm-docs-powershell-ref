---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/31/2021
online version:
schema: 2.0.0
---

# New-CMTSStepRunPowerShellScript

## SYNOPSIS

Create the **Run PowerShell Script** step in a task sequence.

## SYNTAX

### ByName (Default)
```
New-CMTSStepRunPowerShellScript -Name <String> [-SuccessCode <Int32[]>] [-Condition <IResultObject[]>]
 [-ContinueOnError] [-Description <String>] [-Disable] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RunScriptFromSource
```
New-CMTSStepRunPowerShellScript [-ExecutionPolicy <ExecutionPolicyType>] -Name <String>
 [-OutputVariableName <String>] [-Parameter <String>] -SourceScript <String> [-SuccessCode <Int32[]>]
 [-TimeoutMins <Int32>] [-UserName <String>] [-UserPassword <SecureString>] [-WorkingDirectory <String>]
 [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>] [-Disable]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RunScriptFromPackage
```
New-CMTSStepRunPowerShellScript [-ExecutionPolicy <ExecutionPolicyType>] -Name <String>
 [-OutputVariableName <String>] -PackageId <String> [-Parameter <String>] -ScriptName <String>
 [-SuccessCode <Int32[]>] [-TimeoutMins <Int32>] [-UserName <String>] [-UserPassword <SecureString>]
 [-WorkingDirectory <String>] [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>]
 [-Disable] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Run PowerShell Script** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Run PowerShell Script](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RunPowerShellScript).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first creates an object for the **Run PowerShell Script** step. It specifies the package with the name of the script to run. It sets the PowerShell execution policy to the most secure **AllSigned** level, which requires the script to be digitally signed.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$step = New-CMTSStepRunPowerShellScript -Name "Run PowerShell Script" -PackageId "XYZ00821" -ScriptName "Add-ContosoBranding.ps1" -ExecutionPolicy AllSigned 

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

### -ExecutionPolicy

Specify the PowerShell execution policy for the scripts you allow to run on the computer. Choose one of the following policies:

- `AllSigned`: Only run scripts signed by a trusted publisher.

- `Undefined`: Don't define any execution policy.

- `Bypass`: Load all configuration files and run all scripts. If you download an unsigned script from the internet, PowerShell doesn't prompt for permission before running the script.

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

Specify the **package ID** for the package that has the PowerShell script. The package doesn't require a program. One package can contain multiple scripts.

This value is a standard package ID, for example `XYZ00821`.

Then use the **ScriptName** parameter to specify the name of the script.

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

Specify the parameters passed to the PowerShell script. These parameters are the same as the PowerShell script parameters on the command line. Provide parameters consumed by the script, not for the PowerShell command line.

The following example contains _valid_ parameters:

`-MyParameter1 MyValue1 -MyParameter2 MyValue2`

The following example contains _invalid_ parameters. The first two items are PowerShell command-line parameters (**NoLogo** and **ExecutionPolicy**). The script doesn't consume these parameters.

`-NoLogo -ExecutionPolicy Unrestricted -File MyScript.ps1 -MyParameter1 MyValue1 -MyParameter2 MyValue2`

If a parameter value includes a special character or a space, use single quotation marks (`'`) around the value. Using double quotation marks (`"`) may cause the task sequence step to incorrectly process the parameter.

For example: `-Arg1 '%TSVar1%' -Arg2 '%TSVar2%'`

You can also set this parameter to a task sequence variable. For example, if you specify `%MyScriptVariable%`, when the task sequence runs the script, it adds the value of this custom variable to the PowerShell command line.

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

Specify the name of the script to run. This script is in the package specified by the **PackageId** parameter.

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

Instead of using the **PackageId** and **ScriptName** parameters, use this parameter to directly specify the script commands. This string value is the PowerShell commands that this step runs.

You can read the contents of an existing script file into a string variable, and then use that variable for this parameter. For example:

`$script = [IO.File]::ReadAllText( "C:\temp\script.ps1" )`

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

Specify an array of integer values as exit codes from the script that the step should evaluate as success.

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

Specify an integer value that represents how long Configuration Manager allows the script to run. This value can be from `1` minute to `999` minutes. The default value is `15` minutes.

If you enter a value that doesn't allow enough time for the specified script to complete successfully, this step fails. The entire task sequence could fail depending on step or group conditions. If the timeout expires, Configuration Manager terminates the PowerShell process.

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

Use this parameter to run the script as a Windows user account and not the local system account. Specify the name of the Windows user account. To specify the account password, use the **UserPassword** parameter.

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

Use this parameter to specify the password of the account that you specify with **UserName**.

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

Specify the folder in which the command starts. This path can be up to 127 characters.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_RunPowerShellScriptAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_RunPowerShellScriptAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_runpowershellscriptaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepRunPowerShellScript](Get-CMTSStepRunPowerShellScript.md)
[Remove-CMTSStepRunPowerShellScript](Remove-CMTSStepRunPowerShellScript.md)
[Set-CMTSStepRunPowerShellScript](Set-CMTSStepRunPowerShellScript.md)

[About task sequence steps: Run PowerShell Script](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_RunPowerShellScript)
