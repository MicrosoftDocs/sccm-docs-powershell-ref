---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
ms.date: 07/31/2020
schema: 2.0.0
---

# New-CMTSStepPrestartCheck

## SYNOPSIS

Add the **Check Readiness** step to a task sequence. Use this step to verify that the target computer meets the specified deployment prerequisite conditions.

## SYNTAX

```
New-CMTSStepPrestartCheck [-CheckSpace <Boolean>] [-DiskSpace <Int32>] [-CheckPowerState <Boolean>]
 [-CheckUefi <Boolean>] [-CheckNetworkConnected <Boolean>] [-CheckNetworkWired <Boolean>]
 [-CheckMemory <Boolean>] [-Memory <Int32>] [-CheckOSLanguageId <Boolean>] [-OSLanguageId <Int32>]
 [-CheckOS <Boolean>] [-OS <OSType>] [-CheckOSArchitecture <Boolean>] [-OSArchitecture <OSArch>]
 [-CheckMinOSVersion <Boolean>] [-MinOSVersion <String>] [-CheckMaxOSVersion <Boolean>]
 [-MaxOSVersion <String>] [-CheckCMClientMinVersion <Boolean>] [-CMClientMinVersion <String>]
 [-CheckSpeed <Boolean>] [-Speed <Int32>] -Name <String> [-Description <String>] [-ContinueOnError] [-Disable]
 [-Condition <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Add the **Check Readiness** step to a task sequence. Use this step to verify that the target computer meets the specified deployment prerequisite conditions. For more information on this task sequence step, see [About task sequence steps](https://docs.microsoft.com/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CheckReadiness).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

{{ Add example description here }}

```powershell
{{ Add example code here }}
```

## PARAMETERS

### -CheckCMClientMinVersion
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Minimum client version**. Use the parameter **CMClientMinVersion** to set the specific client version number.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Maximum OS version**. Use the parameter **MaxOSVersion** to set the specific OS version number.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Minimum memory (MB)**. Use the parameter **Memory** to set the specific memory size.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Minimum OS version**. Use the parameter **MinOSVersion** to set the specific OS version number.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Network adapter connected**

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Network adapter is not wireless**

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Current OS to be refreshed is**. Use the parameter **OS** to set the specific OS type.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Architecture of current OS**. Use the parameter **OSArchitecture** to set the specific architecture type.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Language of current OS**. Use the parameter **OSLanguageID** to set the specific language.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **AC power plugged in**.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Minimum free disk space (MB)**. Use the parameter **DiskSpace** to set the specific size.

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
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Minimum processor speed (MHz)**. Use the parameter **Speed** to set the specific speed.

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

### -CheckUefi
Applies to version 2006 and later. Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Computer is in UEFI mode**.

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
Specify a condition object to use with this step.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_PrestartCheckAction

## NOTES

## RELATED LINKS

[About task sequence steps - Check Readiness](https://docs.microsoft.com/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CheckReadiness)
