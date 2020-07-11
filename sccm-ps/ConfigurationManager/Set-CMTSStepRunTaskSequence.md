---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMTSStepRunTaskSequence

## SYNOPSIS

Use this cmdlet to edit the task sequence step **Run Task Sequence**.

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepRunTaskSequence [-RunTaskSequence <IResultObject>] -InputObject <IResultObject>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>]
 [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Set-CMTSStepRunTaskSequence [-RunTaskSequence <IResultObject>] -TaskSequenceId <String> [-StepName <String>]
 [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>] [-MoveToIndex <Int32>]
 [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Set-CMTSStepRunTaskSequence [-RunTaskSequence <IResultObject>] -TaskSequenceName <String> [-StepName <String>]
 [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>] [-MoveToIndex <Int32>]
 [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionIfStatement] [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionQueryWmi] [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionVariable] [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>]
 [-ConditionVariableValue <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionOperatingSystem] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionFile] [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionFolder] [-FolderPath <String>] [-FolderTimestamp <DateTime>]
 [-FolderDateTimeOperator <VariableOperatorType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionRegistry] [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueName <String>] [-ValueType <RegistryValueType>]
 [-RegistryValueData <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionSoftware] [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionIfStatement] [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionQueryWmi] [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionVariable] [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>]
 [-ConditionVariableValue <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionOperatingSystem] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionFile] [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionFolder] [-FolderPath <String>] [-FolderTimestamp <DateTime>]
 [-FolderDateTimeOperator <VariableOperatorType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionRegistry] [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueName <String>] [-ValueType <RegistryValueType>]
 [-RegistryValueData <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionSoftware] [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionIfStatement] [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionQueryWmi] [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionVariable] [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>]
 [-ConditionVariableValue <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionOperatingSystem] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionFile] [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionFolder] [-FolderPath <String>] [-FolderTimestamp <DateTime>]
 [-FolderDateTimeOperator <VariableOperatorType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionRegistry] [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueName <String>] [-ValueType <RegistryValueType>]
 [-RegistryValueData <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepRunTaskSequence -RunTaskSequence <IResultObject> -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionSoftware] [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1906, use this cmdlet to edit the task sequence step **Run Task Sequence**.

## EXAMPLES

### Example 1: Change the child task sequence to run

This example gets objects for both task sequences. It then changes the child task sequence that's run from the **Run Task Sequence** step in the parent task sequence.

```powershell
$parentTS = Get-CMTaskSequence -Name "parent task sequence"
$childTS = Get-CMTaskSequence -Name "child task sequence"
$parentTS | Set-CMTSStepRunTaskSequence -RunTaskSequence $childTS
```

## PARAMETERS

### -AddCondition

Specify a task sequence step condition object to add to the specified task sequence. For example, use the [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md) cmdlet.

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

### -ClearCondition

Remove the specified condition from the task sequence step.

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

Specify a task sequence step condition object. For example, use the [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md) cmdlet.

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

Specify the variable name to add as a condition to the task sequence step.

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

Specify the variable value to add as a condition to the task sequence step.

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

Specify a description for the task sequence step.

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

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

Specify an object for the task sequence to modify.

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

Check whether this task sequence step is configured to continue on error.

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

Check whether this task sequence step is enabled.

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

Move the specified task sequence step to the specified integer index.

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

Specify a new name for this task sequence step.

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

### -RunTaskSequence

Specify an object for the child task sequence to run with this step.

```yaml
Type: IResultObject
Parameter Sets: ByValue, ById, ByName
Aliases: Child

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: IResultObject
Parameter Sets: ByIdSetConditionIfStatement, ByIdSetConditionQueryWmi, ByIdSetConditionVariable, ByIdSetConditionOperatingSystem, ByIdSetConditionFile, ByIdSetConditionFolder, ByIdSetConditionRegistry, ByIdSetConditionSoftware, ByNameSetConditionIfStatement, ByNameSetConditionQueryWmi, ByNameSetConditionVariable, ByNameSetConditionOperatingSystem, ByNameSetConditionFile, ByNameSetConditionFolder, ByNameSetConditionRegistry, ByNameSetConditionSoftware, ByValueSetConditionIfStatement, ByValueSetConditionQueryWmi, ByValueSetConditionVariable, ByValueSetConditionOperatingSystem, ByValueSetConditionFile, ByValueSetConditionFolder, ByValueSetConditionRegistry, ByValueSetConditionSoftware
Aliases: Child

Required: True
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

Specify the name of the target task sequence step.

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

Specify the ID of the task sequence to target.

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

Specify the name of the task sequence to target.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
