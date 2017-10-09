---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-CMTSStepInstallApplication

## SYNOPSIS
Sets a t s step install application

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepInstallApplication [-Application <IResultObject[]>] [-BaseVariableName <String>]
 [-EnableContinueOnInstallError <Boolean>] [-RetryCount <Int32>] -InputObject <IResultObject>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-RemoveConditionIfStatement]
 [-RemoveConditionQueryWmi] [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile]
 [-RemoveConditionFolder] [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMTSStepInstallApplication [-Application <IResultObject[]>] [-BaseVariableName <String>]
 [-EnableContinueOnInstallError <Boolean>] [-RetryCount <Int32>] -TaskSequenceId <String> [-StepName <String>]
 [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi]
 [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder]
 [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMTSStepInstallApplication [-Application <IResultObject[]>] [-BaseVariableName <String>]
 [-EnableContinueOnInstallError <Boolean>] [-RetryCount <Int32>] -TaskSequenceName <String>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-RemoveConditionIfStatement]
 [-RemoveConditionQueryWmi] [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile]
 [-RemoveConditionFolder] [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepInstallApplication -TaskSequenceId <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepInstallApplication -TaskSequenceId <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepInstallApplication -TaskSequenceId <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepInstallApplication -TaskSequenceId <String> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepInstallApplication -TaskSequenceId <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepInstallApplication -TaskSequenceId <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepInstallApplication -TaskSequenceId <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepInstallApplication -TaskSequenceId <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepInstallApplication -TaskSequenceName <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepInstallApplication -TaskSequenceName <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepInstallApplication -TaskSequenceName <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepInstallApplication -TaskSequenceName <String> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepInstallApplication -TaskSequenceName <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepInstallApplication -TaskSequenceName <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepInstallApplication -TaskSequenceName <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepInstallApplication -TaskSequenceName <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepInstallApplication -InputObject <IResultObject> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepInstallApplication -InputObject <IResultObject> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepInstallApplication -InputObject <IResultObject> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepInstallApplication -InputObject <IResultObject> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepInstallApplication -InputObject <IResultObject> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepInstallApplication -InputObject <IResultObject> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepInstallApplication -InputObject <IResultObject> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepInstallApplication -InputObject <IResultObject> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddCondition
{{Fill AddCondition Description}}

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

### -Application
{{Fill Application Description}}

```yaml
Type: IResultObject[]
Parameter Sets: ByValue, ById, ByName
Aliases: Applications

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BaseVariableName
{{Fill BaseVariableName Description}}

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
{{Fill ClearCondition Description}}

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
{{Fill Condition Description}}

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
{{Fill ConditionVariableName Description}}

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
{{Fill ConditionVariableValue Description}}

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
{{Fill Description Description}}

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
{{Fill EnableContinueOnInstallError Description}}

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
{{Fill FileDateTimeOperator Description}}

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
{{Fill FilePath Description}}

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
{{Fill FileTimestamp Description}}

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
{{Fill FileVersion Description}}

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
{{Fill FolderDateTimeOperator Description}}

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
{{Fill FolderPath Description}}

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
{{Fill FolderTimestamp Description}}

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
{{Fill InputObject Description}}

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
{{Fill IsAnyVersion Description}}

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
{{Fill IsContinueOnError Description}}

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
{{Fill IsEnabled Description}}

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

### -MsiFilePath
{{Fill MsiFilePath Description}}

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
{{Fill Namespace Description}}

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
{{Fill NewStepName Description}}

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
{{Fill OperatorType Description}}

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
{{Fill Query Description}}

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
{{Fill RegistryKey Description}}

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
{{Fill RegistryOperator Description}}

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
{{Fill RegistryValueData Description}}

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
{{Fill RegistryValueName Description}}

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
{{Fill RemoveConditionFile Description}}

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
{{Fill RemoveConditionFolder Description}}

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
{{Fill RemoveConditionIfStatement Description}}

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
{{Fill RemoveConditionOperatingSystem Description}}

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
{{Fill RemoveConditionQueryWmi Description}}

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
{{Fill RemoveConditionRegistry Description}}

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
{{Fill RemoveConditionSoftware Description}}

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
{{Fill RemoveConditionVariable Description}}

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

### -RetryCount
{{Fill RetryCount Description}}

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

### -RootKey
{{Fill RootKey Description}}

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
{{Fill SetConditionFile Description}}

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
{{Fill SetConditionFolder Description}}

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
{{Fill SetConditionIfStatement Description}}

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
{{Fill SetConditionOperatingSystem Description}}

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
{{Fill SetConditionQueryWmi Description}}

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
{{Fill SetConditionRegistry Description}}

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
{{Fill SetConditionSoftware Description}}

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
{{Fill SetConditionVariable Description}}

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
{{Fill StatementType Description}}

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
{{Fill StepName Description}}

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

### -SupportedPlatform
{{Fill SupportedPlatform Description}}

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
{{Fill TaskSequenceId Description}}

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
{{Fill TaskSequenceName Description}}

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
{{Fill ValueType Description}}

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
{{Fill VersionOperator Description}}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

