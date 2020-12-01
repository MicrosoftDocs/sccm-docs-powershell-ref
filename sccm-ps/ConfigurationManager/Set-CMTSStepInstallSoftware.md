---
description: Sets a TS step install software.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMTSStepInstallSoftware
---

# Set-CMTSStepInstallSoftware

## SYNOPSIS
Sets a TS step install software.

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepInstallSoftware [-BaseVariableName <String>] [-EnableContinueOnInstallError <Boolean>]
 [-Program <IResultObject>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>]
 -InputObject <IResultObject> [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-MoveToIndex <Int32>]
 [-NewStepName <String>] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionIfStatement]
 [-RemoveConditionOperatingSystem] [-RemoveConditionQueryWmi] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-RemoveConditionVariable] [-StepName <String>] [-StepOrder <ReorderType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMTSStepInstallSoftware [-BaseVariableName <String>] [-EnableContinueOnInstallError <Boolean>]
 [-Program <IResultObject>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>]
 [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-MoveToIndex <Int32>] [-NewStepName <String>]
 [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionIfStatement]
 [-RemoveConditionOperatingSystem] [-RemoveConditionQueryWmi] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-RemoveConditionVariable] [-StepName <String>] [-StepOrder <ReorderType>]
 -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Set-CMTSStepInstallSoftware [-BaseVariableName <String>] [-EnableContinueOnInstallError <Boolean>]
 [-Program <IResultObject>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>]
 [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-MoveToIndex <Int32>] [-NewStepName <String>]
 [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionIfStatement]
 [-RemoveConditionOperatingSystem] [-RemoveConditionQueryWmi] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-RemoveConditionVariable] [-StepName <String>] [-StepOrder <ReorderType>]
 -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepInstallSoftware [-Condition <IResultObject[]>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepInstallSoftware [-Condition <IResultObject[]>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepInstallSoftware [-Condition <IResultObject[]>] -InputObject <IResultObject>
 [-SetConditionIfStatement] [-StatementType <ConditionStatementType>] [-StepName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepInstallSoftware [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-OperatorType <VariableOperatorType>] [-SetConditionVariable] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepInstallSoftware [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-OperatorType <VariableOperatorType>] [-SetConditionVariable] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepInstallSoftware [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 -InputObject <IResultObject> [-OperatorType <VariableOperatorType>] [-SetConditionVariable]
 [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepInstallSoftware [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] [-SetConditionFile] [-StepName <String>]
 -TaskSequenceId <String> [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepInstallSoftware [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] [-SetConditionFile] [-StepName <String>]
 -TaskSequenceName <String> [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepInstallSoftware [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] -InputObject <IResultObject> [-SetConditionFile]
 [-StepName <String>] [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepInstallSoftware [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] [-SetConditionFolder] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepInstallSoftware [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] [-SetConditionFolder] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepInstallSoftware [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] -InputObject <IResultObject> [-SetConditionFolder] [-StepName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepInstallSoftware -InputObject <IResultObject> [-Namespace <String[]>] [-Query <String>]
 [-SetConditionQueryWmi] [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepInstallSoftware -InputObject <IResultObject> [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepInstallSoftware -InputObject <IResultObject> [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueData <String>] [-RegistryValueName <String>]
 [-RootKey <RegistryRootKeyType>] [-SetConditionRegistry] [-StepName <String>] [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepInstallSoftware -InputObject <IResultObject> [-IsAnyVersion <Boolean>] [-MsiFilePath <String>]
 [-SetConditionSoftware] [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepInstallSoftware [-IsAnyVersion <Boolean>] [-MsiFilePath <String>] [-SetConditionSoftware]
 [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepInstallSoftware [-IsAnyVersion <Boolean>] [-MsiFilePath <String>] [-SetConditionSoftware]
 [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepInstallSoftware [-Namespace <String[]>] [-Query <String>] [-SetConditionQueryWmi]
 [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepInstallSoftware [-Namespace <String[]>] [-Query <String>] [-SetConditionQueryWmi]
 [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepInstallSoftware [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueData <String>] [-RegistryValueName <String>] [-RootKey <RegistryRootKeyType>]
 [-SetConditionRegistry] [-StepName <String>] -TaskSequenceId <String> [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepInstallSoftware [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueData <String>] [-RegistryValueName <String>] [-RootKey <RegistryRootKeyType>]
 [-SetConditionRegistry] [-StepName <String>] -TaskSequenceName <String> [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepInstallSoftware [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] -TaskSequenceId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepInstallSoftware [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -AddCondition
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

### -BaseVariableName
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

### -ClearCondition
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

### -Description
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

### -EnableContinueOnInstallError
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

### -FileDateTimeOperator
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
```yaml
Type: IResultObject
Parameter Sets: ByValue, ByValueSetConditionIfStatement, ByValueSetConditionVariable, ByValueSetConditionFile, ByValueSetConditionFolder, ByValueSetConditionQueryWmi, ByValueSetConditionOperatingSystem, ByValueSetConditionRegistry, ByValueSetConditionSoftware
Aliases: TaskSequence

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsAnyVersion
```yaml
Type: Boolean
Parameter Sets: ByValueSetConditionSoftware, ByIdSetConditionSoftware, ByNameSetConditionSoftware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsContinueOnError
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
Move this step to the specified index position in the task sequence.

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
```yaml
Type: String
Parameter Sets: ByValueSetConditionSoftware, ByIdSetConditionSoftware, ByNameSetConditionSoftware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
```yaml
Type: String[]
Parameter Sets: ByValueSetConditionQueryWmi, ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewStepName
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

### -Program
```yaml
Type: IResultObject
Parameter Sets: ByValue, ById, ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
```yaml
Type: String
Parameter Sets: ByValueSetConditionQueryWmi, ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryKey
```yaml
Type: String
Parameter Sets: ByValueSetConditionRegistry, ByIdSetConditionRegistry, ByNameSetConditionRegistry
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryOperator
```yaml
Type: VariableOperatorType
Parameter Sets: ByValueSetConditionRegistry, ByIdSetConditionRegistry, ByNameSetConditionRegistry
Aliases:
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryValueData
```yaml
Type: String
Parameter Sets: ByValueSetConditionRegistry, ByIdSetConditionRegistry, ByNameSetConditionRegistry
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryValueName
```yaml
Type: String
Parameter Sets: ByValueSetConditionRegistry, ByIdSetConditionRegistry, ByNameSetConditionRegistry
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveConditionFile
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
```yaml
Type: RegistryRootKeyType
Parameter Sets: ByValueSetConditionRegistry, ByIdSetConditionRegistry, ByNameSetConditionRegistry
Aliases:
Accepted values: HKeyCurrentUser, HKeyLocalMachine, HKeyUsers, HKeyCurrentConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionFile
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
```yaml
Type: SwitchParameter
Parameter Sets: ByValueSetConditionOperatingSystem, ByIdSetConditionOperatingSystem, ByNameSetConditionOperatingSystem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionQueryWmi
```yaml
Type: SwitchParameter
Parameter Sets: ByValueSetConditionQueryWmi, ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionRegistry
```yaml
Type: SwitchParameter
Parameter Sets: ByValueSetConditionRegistry, ByIdSetConditionRegistry, ByNameSetConditionRegistry
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionSoftware
```yaml
Type: SwitchParameter
Parameter Sets: ByValueSetConditionSoftware, ByIdSetConditionSoftware, ByNameSetConditionSoftware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetConditionVariable
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
Use this parameter to reorder the step in the task sequence.

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
```yaml
Type: IResultObject[]
Parameter Sets: ByValueSetConditionOperatingSystem, ByIdSetConditionOperatingSystem, ByNameSetConditionOperatingSystem
Aliases: SupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceId
```yaml
Type: String
Parameter Sets: ById, ByIdSetConditionIfStatement, ByIdSetConditionVariable, ByIdSetConditionFile, ByIdSetConditionFolder, ByIdSetConditionSoftware, ByIdSetConditionQueryWmi, ByIdSetConditionRegistry, ByIdSetConditionOperatingSystem
Aliases: Id, TaskSequencePackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName
```yaml
Type: String
Parameter Sets: ByName, ByNameSetConditionIfStatement, ByNameSetConditionVariable, ByNameSetConditionFile, ByNameSetConditionFolder, ByNameSetConditionSoftware, ByNameSetConditionQueryWmi, ByNameSetConditionRegistry, ByNameSetConditionOperatingSystem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueType
```yaml
Type: RegistryValueType
Parameter Sets: ByValueSetConditionRegistry, ByIdSetConditionRegistry, ByNameSetConditionRegistry
Aliases:
Accepted values: RegistrySZ, RegistryExpandSZ, RegistryDWord

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VersionOperator
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
