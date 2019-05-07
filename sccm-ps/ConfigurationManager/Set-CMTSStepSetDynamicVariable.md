---
title: Set-CMTSStepSetDynamicVariable
titleSuffix: Configuration Manager
description: Sets properties, options, specific conditions for a task sequence Set Dynamic Variable step in Configuration Manager. 
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Set-CMTSStepSetDynamicVariable

## SYNOPSIS

Sets properties, options, specific conditions for a task sequence Set Dynamic Variable step in Configuration Manager. 

## SYNTAX

### ByValue (Default)

```powershell
Set-CMTSStepSetDynamicVariable [-AddRule <IResultObject[]>] [-CleanRule] -InputObject <IResultObject>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>]
 [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ById

```powershell
Set-CMTSStepSetDynamicVariable [-AddRule <IResultObject[]>] [-CleanRule] -TaskSequenceId <String>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>]
 [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByName

```powershell
Set-CMTSStepSetDynamicVariable [-AddRule <IResultObject[]>] [-CleanRule] -TaskSequenceName <String>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>]
 [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByIdSetConditionIfStatement

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceId <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByIdSetConditionQueryWmi

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceId <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm]
```

### ByIdSetConditionVariable

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceId <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByIdSetConditionOperatingSystem

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceId <String> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm]
```

### ByIdSetConditionFile

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceId <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByIdSetConditionFolder

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceId <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByIdSetConditionRegistry

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceId <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByIdSetConditionSoftware

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceId <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm]
```

### ByNameSetConditionIfStatement

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceName <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByNameSetConditionQueryWmi

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceName <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm]
```

### ByNameSetConditionVariable

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceName <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByNameSetConditionOperatingSystem

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceName <String> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm]
```

### ByNameSetConditionFile

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceName <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByNameSetConditionFolder

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceName <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByNameSetConditionRegistry

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceName <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByNameSetConditionSoftware

```powershell
Set-CMTSStepSetDynamicVariable -TaskSequenceName <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm]
```

### ByValueSetConditionIfStatement

```powershell
Set-CMTSStepSetDynamicVariable -InputObject <IResultObject> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByValueSetConditionQueryWmi

```powershell
Set-CMTSStepSetDynamicVariable -InputObject <IResultObject> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm]
```

### ByValueSetConditionVariable

```powershell
Set-CMTSStepSetDynamicVariable -InputObject <IResultObject> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByValueSetConditionOperatingSystem

```powershell
Set-CMTSStepSetDynamicVariable -InputObject <IResultObject> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm]
```

### ByValueSetConditionFile

```powershell
Set-CMTSStepSetDynamicVariable -InputObject <IResultObject> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByValueSetConditionFolder

```powershell
Set-CMTSStepSetDynamicVariable -InputObject <IResultObject> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByValueSetConditionRegistry

```powershell
Set-CMTSStepSetDynamicVariable -InputObject <IResultObject> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### ByValueSetConditionSoftware

```powershell
Set-CMTSStepSetDynamicVariable -InputObject <IResultObject> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm]
```

## DESCRIPTION

The **Set-CMTSStepSetDynamicVariable** cmdlet sets properties, options, specific conditions for â€œSet Dynamic Variableâ€ steps in a task sequence.  The cmdlet supports pipeline from a task sequence object, and could be filtered by the name of the step.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1

```powershell
PS XYZ:\> $ReferencedTaskSequence | Set-CMTaskSequenceStepSetDynamicVariable -ClearCondition -AddCondition $cd1 -CleanRule -AddRule ($rule5,$rule6)
```

## PARAMETERS

### -AddCondition

Specifies the conditions. The types of the conditions include: task sequence variable, operating system version, operating system language, file properties, folder properties, registry setting, query WMI, and installed software.

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

### -AddRule

Specifies the rules and the order of the rules.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue, ById, ByName
Aliases: AddRules

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanRule

Indicates removing all the existing rules. This parameter must be used in conjunction with the **AddRule** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases: CleanRules

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearCondition

Indicates removing all the existing conditions.

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

### -Condition

Specifies the conditions. This parameter is used with one of the following parameters: SetConditionIfStatement, SetConditionQueryWmi, SetConditionVariable, SetConditionOperatingSystem, SetConditionFile, SetConditionFolder, SetConditionRegistry, and SetConditionSoftware. 

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

Specifies a condition variable name.

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

Specifies condition variable value.

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

Specifies a description.

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

### -FileDateTimeOperator

Specifies a file date time operator.

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

Specifies a file path.

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

Specifies a file time stamp.

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

Specifies a file version.

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

Specifies a folder date time operator.

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

Specifies a folder path.

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

Specifies a folder time stamp.

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

### -InputObject

Specifies a task sequence object.

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

Indicates whether you want to match any version of the product (upgrade code only). This is parameter is used for the Software condition.

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

Indicates the command continues when there is an exception.

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

Indicates whether this step can be ran.

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

### -MoveToIndex

Specifies the order of this step. The order index is 0 based. This parameter must be used in conjunction with the **StepOrder** parameter.

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

Specifies an MSI file path.

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

Specifies a WMI namespace. This parameter is used for the Query WMI condition.

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

Specifies a new step name.

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

Specifies an operator type.

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

### -Query

Specifies a query.

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

Specifies a registry key.

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

Specifies a registry operator.

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

Specifies registry value data.

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

Specifies registry value name.

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

Indicates removing the conditions of the File Properties type.

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

Indicates removing the conditions of the Folder Properties type.

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

Indicates removing the conditions of the If Statement type.

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

Indicates removing the conditions of the Operating System type.

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

Indicates removing the conditions of the Query WMI type.

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

Indicates removing the conditions of the Registry Setting type.

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

Indicates removing the conditions of the Installed Software type.

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

Indicates removing the conditions of the Task Sequence Variable type.

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

Specifies a root key of a Registry Setting type condition.

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

Indicate setting all the conditions of the File Properties type.

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

Indicate setting all the conditions of the Folder Properties type.

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

Indicate setting all the conditions of the If Statement type.

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

Indicate setting all the conditions of the Operating System type.

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

Indicate setting all the conditions of the Query WMI type.

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

Indicate setting all the conditions of the Registry Setting type.

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

Indicate setting all the conditions of the Installed Software type.

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

Indicate setting all the conditions of the Task Sequence Variable type.

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

### -StatementType

Specifies a statement type.

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

Specifies a step name.

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

Specifies the order of a step. If MoveToIndex is specified, you must also specify the MoveToIndex parameter.

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

Specifies supported platforms.

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

Specifies a task sequence ID.

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

Specifies a task sequence name.

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

Specifies a value type.

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

Specifies a version operator.

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

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## RELATED LINKS

[New-CMTSStepSetDynamicVariable](./New-CMTSStepSetDynamicVariable.md)

[Get-CMTSStepSetDynamicVariable](./Get-CMTSStepSetDynamicVariable.md)

[Remove-CMTSStepSetDynamicVariable](./Remove-CMTSStepSetDynamicVariable.md)
