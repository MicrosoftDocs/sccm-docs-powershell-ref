---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2021
online version:
schema: 2.0.0
---

# New-CMTSStepPrestartCheck

## SYNOPSIS

Create a **Check Readiness** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepPrestartCheck [-CheckCMClientMinVersion <Boolean>] [-CheckMaxOSVersion <Boolean>]
 [-CheckMemory <Boolean>] [-CheckMinOSVersion <Boolean>] [-CheckNetworkConnected <Boolean>]
 [-CheckNetworkWired <Boolean>] [-CheckTpmEnabled <Boolean>] [-CheckTpmActivated <Boolean>]
 [-CheckOS <Boolean>] [-CheckOSArchitecture <Boolean>] [-CheckOSLanguageId <Boolean>]
 [-CheckPowerState <Boolean>] [-CheckSpace <Boolean>] [-CheckSpeed <Boolean>] [-CheckUefi <Boolean>]
 [-CMClientMinVersion <String>] [-DiskSpace <Int32>] [-MaxOSVersion <String>] [-Memory <Int32>]
 [-MinOSVersion <String>] [-OS <OSType>] [-OSArchitecture <OSArch>] [-OSLanguageId <Int32>] [-Speed <Int32>]
 [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>] [-Disable] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Check Readiness** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Check Readiness](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CheckReadiness).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first [splats](/powershell/module/microsoft.powershell.core/about/about_splatting) the cmdlet parameters into the **parameters** variable.

Next it creates an object for the **Check Readiness** step, passing the collection of values in **parameters**.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$parameters = @{
  Name = "Check Readiness"
  CheckMemory = $true
  Memory = 4096
  CheckSpeed = $true
  Speed = 1024
  CheckSpace = $true
  DiskSpace = 512000
  CheckOS = $true
  OS = "Client"
  CheckOSArchitecture = $true
  OSArchitecture = "Arch64"
  CheckMinOSVersion = $true
  MinOSVersion = "10.0.16299"
  CheckMaxOSVersion = $true
  MaxOSVersion = "10.0.99999"
  CheckCMClientMinVersion = $true
  CMClientMinVersion = "5.00.8913.1005"
  CheckOSLanguageId = $true
  OSLanguageID = 1033
  CheckPowerState = $true
  CheckNetworkConnected = $true
  CheckNetworkWired = $false
  CheckUefi = $true
}

$step = New-CMTSStepPrestartCheck @parameters

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -CheckCMClientMinVersion

Set this parameter to `$true` to enable the **Minimum client version** check. Use the parameter **CMClientMinVersion** to set the specific client version number.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CheckClientMinVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckMaxOSVersion

Set this parameter to `$true` to enable the **Maximum OS version** check. Use the parameter **MaxOSVersion** to set the specific OS version number.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckMaxOSVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckMemory

Set this parameter to `$true` to enable the **Minimum memory (MB)** check. Use the parameter **Memory** to set the specific memory size.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckMemory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckMinOSVersion

Set this parameter to `$true` to enable the **Minimum OS version** check. Use the parameter **MinOSVersion** to set the specific OS version number.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckMinOSVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckNetworkConnected

Set this parameter to `$true` to enable the **Network adapter connected** check.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: NetworkConnected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckNetworkWired

Set this parameter to `$true` to enable the **Network adapter is not wireless** check.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: NetworkWired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckOS

Set this parameter to `$true` to enable the check for the type of OS, either client or server. Use the parameter **OS** to set the specific OS type.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckOSType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckOSArchitecture

Set this parameter to `$true` to enable the **Architecture of current OS** check. Use the parameter **OSArchitecture** to set the specific architecture type.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckOSArchitecture

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckOSLanguageId

Set this parameter to `$true` to enable the check of the **Language of current OS**. Use the parameter **OSLanguageID** to set the specific language.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableOSLanguageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckPowerState

Set this parameter to `$true` to enable the **AC power plugged in** check.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: NotBattery

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckSpace

Set this parameter to `$true` to enable the **Minimum free disk space (MB)** check. Use the parameter **DiskSpace** to set the specific size.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckFreeDiskSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckSpeed

Set this parameter to `$true` to enable the **Minimum processor speed (MHz)** check. Use the parameter **Speed** to set the specific speed.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCheckProcessorSpeed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckTpmActivated
{{ Fill CheckTpmActivated Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: TpmActivated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckTpmEnabled
{{ Fill CheckTpmEnabled Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: TpmEnabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckUefi

Applies to version 2006 and later. Set this parameter to `$true` to enable the **Computer is in UEFI mode** check.

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

### -CMClientMinVersion

Use this parameter to configure the specific client version. Specify the client version in the following format: `5.00.8913.1005`. Use the parameter **CheckCMClientMinVersion** to enable or disable the check.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClientMinVersion

Required: False
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

### -DiskSpace

Use this parameter to configure the specific size for the minimum free disk space check. Specify an integer value for the size in MB. Use the parameter **CheckSpace** to enable or disable the check.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinimumFreeDiskSpace

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

### -MaxOSVersion

Use this parameter to configure the specific OS version. Specify the maximum OS version with major version, minor version, and build number. For example, `10.0.18356`. Use the parameter **CheckMaxOSVersion** to enable or disable the check.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CurrentMaxOSVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Memory

Use this parameter to configure the specific size for the minimum memory check. Specify an integer value for the size in MB. Use the parameter **CheckMemory** to enable or disable the check.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinimumMemory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinOSVersion

Use this parameter to configure the specific OS version. Specify the minimum OS version with major version, minor version, and build number. For example, `10.0.16299`. Use the parameter **CheckMinOSVersion** to enable or disable the check.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CurrentMinOSVersion

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

### -OS

Use this parameter to configure the specific OS type: `Client` or `Server`. Use the parameter **CheckOS** to enable or disable the check.

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: CurrentOSType
Accepted values: Client, Server

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSArchitecture

Use this parameter to configure the specific OS architecture: `Arch32` for 32-bit or `Arch64` for 64-bit. Use the parameter **CheckOSArchitecture** to enable or disable the check.

```yaml
Type: OSArch
Parameter Sets: (All)
Aliases: CurrentOSArchitecture
Accepted values: Arch32, Arch64

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSLanguageId

Use this parameter to configure the specific OS language. This check compares the language ID to the **OSLanguage** property of the **Win32_OperatingSystem** WMI class on the client. For example, `1033` for **English (United States)**. Use the parameter **CheckOSLanguageId** to enable or disable the check.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: LanguageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Speed

Use this parameter to configure the specific speed for the minimum processor speed check. Specify an integer value for the speed in MHz. Use the parameter **CheckSpeed** to enable or disable the check.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinimumProcessorSpeed

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

### IResultObject#SMS_TaskSequence_PrestartCheckAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_PrestartCheckAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_prestartcheckaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepPrestartCheck](Get-CMTSStepPrestartCheck.md)
[Remove-CMTSStepPrestartCheck](Remove-CMTSStepPrestartCheck.md)
[Set-CMTSStepPrestartCheck](Set-CMTSStepPrestartCheck.md)

[About task sequence steps: Check Readiness](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CheckReadiness)
