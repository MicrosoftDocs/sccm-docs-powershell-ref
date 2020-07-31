---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMTSStepPrestartCheck

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepPrestartCheck [-CheckSpace <Boolean>] [-DiskSpace <Int32>] [-CheckMemory <Boolean>]
 [-Memory <Int32>] [-CheckOSLanguageId <Boolean>] [-OSLanguageId <Int32>] [-CheckPowerState <Boolean>]
 [-CheckOSArchitecture <Boolean>] [-CheckMinOSVersion <Boolean>] [-MinOSVersion <String>]
 [-CheckMaxOSVersion <Boolean>] [-MaxOSVersion <String>] [-CheckCMClientMinVersion <Boolean>]
 [-CMClientMinVersion <String>] [-CheckNetworkConnected <Boolean>] [-CheckNetworkWired <Boolean>]
 [-CheckOS <Boolean>] [-OS <OSType>] [-OSArchitecture <OSArch>] [-CheckSpeed <Boolean>] [-Speed <Int32>]
 -InputObject <IResultObject> [-StepName <String>] [-NewStepName <String>] [-Description <String>]
 [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition]
 [-StepOrder <ReorderType>] [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi]
 [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder]
 [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMTSStepPrestartCheck [-CheckSpace <Boolean>] [-DiskSpace <Int32>] [-CheckMemory <Boolean>]
 [-Memory <Int32>] [-CheckOSLanguageId <Boolean>] [-OSLanguageId <Int32>] [-CheckPowerState <Boolean>]
 [-CheckOSArchitecture <Boolean>] [-CheckMinOSVersion <Boolean>] [-MinOSVersion <String>]
 [-CheckMaxOSVersion <Boolean>] [-MaxOSVersion <String>] [-CheckCMClientMinVersion <Boolean>]
 [-CMClientMinVersion <String>] [-CheckNetworkConnected <Boolean>] [-CheckNetworkWired <Boolean>]
 [-CheckOS <Boolean>] [-OS <OSType>] [-OSArchitecture <OSArch>] [-CheckSpeed <Boolean>] [-Speed <Int32>]
 -TaskSequenceId <String> [-StepName <String>] [-NewStepName <String>] [-Description <String>]
 [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition]
 [-StepOrder <ReorderType>] [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi]
 [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder]
 [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMTSStepPrestartCheck [-CheckSpace <Boolean>] [-DiskSpace <Int32>] [-CheckMemory <Boolean>]
 [-Memory <Int32>] [-CheckOSLanguageId <Boolean>] [-OSLanguageId <Int32>] [-CheckPowerState <Boolean>]
 [-CheckOSArchitecture <Boolean>] [-CheckMinOSVersion <Boolean>] [-MinOSVersion <String>]
 [-CheckMaxOSVersion <Boolean>] [-MaxOSVersion <String>] [-CheckCMClientMinVersion <Boolean>]
 [-CMClientMinVersion <String>] [-CheckNetworkConnected <Boolean>] [-CheckNetworkWired <Boolean>]
 [-CheckOS <Boolean>] [-OS <OSType>] [-OSArchitecture <OSArch>] [-CheckSpeed <Boolean>] [-Speed <Int32>]
 -TaskSequenceName <String> [-StepName <String>] [-NewStepName <String>] [-Description <String>]
 [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition]
 [-StepOrder <ReorderType>] [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi]
 [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder]
 [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepPrestartCheck -TaskSequenceId <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepPrestartCheck -TaskSequenceId <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepPrestartCheck -TaskSequenceId <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepPrestartCheck -TaskSequenceId <String> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepPrestartCheck -TaskSequenceId <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepPrestartCheck -TaskSequenceId <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepPrestartCheck -TaskSequenceId <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepPrestartCheck -TaskSequenceId <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepPrestartCheck -TaskSequenceName <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepPrestartCheck -TaskSequenceName <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepPrestartCheck -TaskSequenceName <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepPrestartCheck -TaskSequenceName <String> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepPrestartCheck -TaskSequenceName <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepPrestartCheck -TaskSequenceName <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepPrestartCheck -TaskSequenceName <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepPrestartCheck -TaskSequenceName <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepPrestartCheck -InputObject <IResultObject> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepPrestartCheck -InputObject <IResultObject> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepPrestartCheck -InputObject <IResultObject> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepPrestartCheck -InputObject <IResultObject> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepPrestartCheck -InputObject <IResultObject> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepPrestartCheck -InputObject <IResultObject> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepPrestartCheck -InputObject <IResultObject> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepPrestartCheck -InputObject <IResultObject> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddCondition
{{ Fill AddCondition Description }}

```yaml
Type: IResultObject[]
Parameter Sets: ByValue, ById, ByName
Aliases: AddConditions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckCMClientMinVersion
Use this parameter to enable or disable the following setting in the **Check Readiness** task sequence step: **Minimum client version**. Use the parameter **CMClientMinVersion** to set the specific client version number.

```yaml
Type: Boolean
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
Aliases:

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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
Aliases:

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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
Aliases:

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
Parameter Sets: ByValue, ById, ByName
Aliases: EnableCheckOSLanguageId

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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
Aliases: EnableCheckProcessorSpeed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearCondition
{{ Fill ClearCondition Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases: ClearConditions

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
Parameter Sets: ByValue, ById, ByName
Aliases: ClientMinVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Condition
{{ Fill Condition Description }}

```yaml
Type: IResultObject[]
Parameter Sets: ByIdSetConditionIfStatement, ByNameSetConditionIfStatement, ByValueSetConditionIfStatement
Aliases: SubCondition, SubConditions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionVariableName
{{ Fill ConditionVariableName Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionVariable, ByNameSetConditionVariable, ByValueSetConditionVariable
Aliases: Variable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionVariableValue
{{ Fill ConditionVariableValue Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionVariable, ByNameSetConditionVariable, ByValueSetConditionVariable
Aliases: Value

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
{{ Fill Description Description }}

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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
Parameter Sets: ByValue, ById, ByName
Aliases: MinimumFreeDiskSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileDateTimeOperator
{{ Fill FileDateTimeOperator Description }}

```yaml
Type: VariableOperatorType
Parameter Sets: ByIdSetConditionFile, ByNameSetConditionFile, ByValueSetConditionFile
Aliases:
Accepted values: Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
{{ Fill FilePath Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionFile, ByNameSetConditionFile, ByValueSetConditionFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileTimestamp
{{ Fill FileTimestamp Description }}

```yaml
Type: DateTime
Parameter Sets: ByIdSetConditionFile, ByNameSetConditionFile, ByValueSetConditionFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileVersion
{{ Fill FileVersion Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionFile, ByNameSetConditionFile, ByValueSetConditionFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FolderDateTimeOperator
{{ Fill FolderDateTimeOperator Description }}

```yaml
Type: VariableOperatorType
Parameter Sets: ByIdSetConditionFolder, ByNameSetConditionFolder, ByValueSetConditionFolder
Aliases:
Accepted values: Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FolderPath
{{ Fill FolderPath Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionFolder, ByNameSetConditionFolder, ByValueSetConditionFolder
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FolderTimestamp
{{ Fill FolderTimestamp Description }}

```yaml
Type: DateTime
Parameter Sets: ByIdSetConditionFolder, ByNameSetConditionFolder, ByValueSetConditionFolder
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
{{ Fill ForceWildcardHandling Description }}

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

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: ByValue, ByValueSetConditionIfStatement, ByValueSetConditionQueryWmi, ByValueSetConditionVariable, ByValueSetConditionOperatingSystem, ByValueSetConditionFile, ByValueSetConditionFolder, ByValueSetConditionRegistry, ByValueSetConditionSoftware
Aliases: TaskSequence

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsAnyVersion
{{ Fill IsAnyVersion Description }}

```yaml
Type: Boolean
Parameter Sets: ByIdSetConditionSoftware, ByNameSetConditionSoftware, ByValueSetConditionSoftware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsContinueOnError
{{ Fill IsContinueOnError Description }}

```yaml
Type: Boolean
Parameter Sets: ByValue, ById, ByName
Aliases: IsThisStepContinueOnError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsEnabled
{{ Fill IsEnabled Description }}

```yaml
Type: Boolean
Parameter Sets: ByValue, ById, ByName
Aliases: IsThisStepEnabled

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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
Aliases: CurrentMinOSVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveToIndex
{{ Fill MoveToIndex Description }}

```yaml
Type: Int32
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MsiFilePath
{{ Fill MsiFilePath Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionSoftware, ByNameSetConditionSoftware, ByValueSetConditionSoftware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
{{ Fill Namespace Description }}

```yaml
Type: String[]
Parameter Sets: ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi, ByValueSetConditionQueryWmi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewStepName
{{ Fill NewStepName Description }}

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatorType
{{ Fill OperatorType Description }}

```yaml
Type: VariableOperatorType
Parameter Sets: ByIdSetConditionVariable, ByNameSetConditionVariable, ByValueSetConditionVariable
Aliases:
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual, Like

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OS
Use this parameter to configure the specific OS type: `Client` or `Server`. Use the parameter **CheckOS** to enable or disable the check.

```yaml
Type: OSType
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
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
Parameter Sets: ByValue, ById, ByName
Aliases: LanguageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
{{ Fill Query Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi, ByValueSetConditionQueryWmi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryKey
{{ Fill RegistryKey Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryOperator
{{ Fill RegistryOperator Description }}

```yaml
Type: VariableOperatorType
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
Aliases:
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryValueData
{{ Fill RegistryValueData Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryValueName
{{ Fill RegistryValueName Description }}

```yaml
Type: String
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionFile
{{ Fill RemoveConditionFile Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionFolder
{{ Fill RemoveConditionFolder Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionIfStatement
{{ Fill RemoveConditionIfStatement Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionOperatingSystem
{{ Fill RemoveConditionOperatingSystem Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionQueryWmi
{{ Fill RemoveConditionQueryWmi Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionRegistry
{{ Fill RemoveConditionRegistry Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionSoftware
{{ Fill RemoveConditionSoftware Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionVariable
{{ Fill RemoveConditionVariable Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RootKey
{{ Fill RootKey Description }}

```yaml
Type: RegistryRootKeyType
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
Aliases:
Accepted values: HKeyCurrentUser, HKeyLocalMachine, HKeyUsers, HKeyCurrentConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionFile
{{ Fill SetConditionFile Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByIdSetConditionFile, ByNameSetConditionFile, ByValueSetConditionFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionFolder
{{ Fill SetConditionFolder Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByIdSetConditionFolder, ByNameSetConditionFolder, ByValueSetConditionFolder
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionIfStatement
{{ Fill SetConditionIfStatement Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByIdSetConditionIfStatement, ByNameSetConditionIfStatement, ByValueSetConditionIfStatement
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionOperatingSystem
{{ Fill SetConditionOperatingSystem Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByIdSetConditionOperatingSystem, ByNameSetConditionOperatingSystem, ByValueSetConditionOperatingSystem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionQueryWmi
{{ Fill SetConditionQueryWmi Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi, ByValueSetConditionQueryWmi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionRegistry
{{ Fill SetConditionRegistry Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionSoftware
{{ Fill SetConditionSoftware Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByIdSetConditionSoftware, ByNameSetConditionSoftware, ByValueSetConditionSoftware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionVariable
{{ Fill SetConditionVariable Description }}

```yaml
Type: SwitchParameter
Parameter Sets: ByIdSetConditionVariable, ByNameSetConditionVariable, ByValueSetConditionVariable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Speed
Use this parameter to configure the specific speed for the minimum processor speed check. Specify an integer value for the speed in MHz. Use the parameter **CheckSpeed** to enable or disable the check.

```yaml
Type: Int32
Parameter Sets: ByValue, ById, ByName
Aliases: MinimumProcessorSpeed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatementType
{{ Fill StatementType Description }}

```yaml
Type: ConditionStatementType
Parameter Sets: ByIdSetConditionIfStatement, ByNameSetConditionIfStatement, ByValueSetConditionIfStatement
Aliases: Operator
Accepted values: All, Any, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StepName
{{ Fill StepName Description }}

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

### -StepOrder
{{ Fill StepOrder Description }}

```yaml
Type: ReorderType
Parameter Sets: ByValue, ById, ByName
Aliases:
Accepted values: MoveUp, MoveDown, MoveToIndex

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportedPlatform
{{ Fill SupportedPlatform Description }}

```yaml
Type: IResultObject[]
Parameter Sets: ByIdSetConditionOperatingSystem, ByNameSetConditionOperatingSystem, ByValueSetConditionOperatingSystem
Aliases: SupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceId
{{ Fill TaskSequenceId Description }}

```yaml
Type: String
Parameter Sets: ById, ByIdSetConditionIfStatement, ByIdSetConditionQueryWmi, ByIdSetConditionVariable, ByIdSetConditionOperatingSystem, ByIdSetConditionFile, ByIdSetConditionFolder, ByIdSetConditionRegistry, ByIdSetConditionSoftware
Aliases: Id, TaskSequencePackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName
{{ Fill TaskSequenceName Description }}

```yaml
Type: String
Parameter Sets: ByName, ByNameSetConditionIfStatement, ByNameSetConditionQueryWmi, ByNameSetConditionVariable, ByNameSetConditionOperatingSystem, ByNameSetConditionFile, ByNameSetConditionFolder, ByNameSetConditionRegistry, ByNameSetConditionSoftware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueType
{{ Fill ValueType Description }}

```yaml
Type: RegistryValueType
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
Aliases:
Accepted values: RegistrySZ, RegistryExpandSZ, RegistryDWord

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VersionOperator
{{ Fill VersionOperator Description }}

```yaml
Type: VariableOperatorType
Parameter Sets: ByIdSetConditionFile, ByNameSetConditionFile, ByValueSetConditionFile
Aliases:
Accepted values: Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
