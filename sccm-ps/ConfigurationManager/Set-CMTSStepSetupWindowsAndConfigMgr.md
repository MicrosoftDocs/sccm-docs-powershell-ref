---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-CMTSStepSetupWindowsAndConfigMgr

## SYNOPSIS
Sets a TS step setup windows and config mgr

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepSetupWindowsAndConfigMgr [-PackageId <String>] [-PreproductionPackageId <String>]
 [-InstallationProperty <String>] -InputObject <IResultObject> [-StepName <String>] [-NewStepName <String>]
 [-Description <String>] [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi]
 [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder]
 [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMTSStepSetupWindowsAndConfigMgr [-PackageId <String>] [-PreproductionPackageId <String>]
 [-InstallationProperty <String>] -TaskSequenceId <String> [-StepName <String>] [-NewStepName <String>]
 [-Description <String>] [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi]
 [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder]
 [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMTSStepSetupWindowsAndConfigMgr [-PackageId <String>] [-PreproductionPackageId <String>]
 [-InstallationProperty <String>] -TaskSequenceName <String> [-StepName <String>] [-NewStepName <String>]
 [-Description <String>] [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi]
 [-RemoveConditionVariable] [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder]
 [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceId <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceId <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceId <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceId <String> [-StepName <String>]
 [-SetConditionOperatingSystem] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceId <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceId <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceId <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceId <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceName <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceName <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceName <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceName <String> [-StepName <String>]
 [-SetConditionOperatingSystem] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceName <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceName <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceName <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepSetupWindowsAndConfigMgr -TaskSequenceName <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepSetupWindowsAndConfigMgr -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionIfStatement] [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepSetupWindowsAndConfigMgr -InputObject <IResultObject> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepSetupWindowsAndConfigMgr -InputObject <IResultObject> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepSetupWindowsAndConfigMgr -InputObject <IResultObject> [-StepName <String>]
 [-SetConditionOperatingSystem] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepSetupWindowsAndConfigMgr -InputObject <IResultObject> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepSetupWindowsAndConfigMgr -InputObject <IResultObject> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepSetupWindowsAndConfigMgr -InputObject <IResultObject> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepSetupWindowsAndConfigMgr -InputObject <IResultObject> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


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
Parameter Sets: ByValue, ByValueSetConditionIfStatement, ByValueSetConditionQueryWmi, ByValueSetConditionVariable, ByValueSetConditionOperatingSystem, ByValueSetConditionFile, ByValueSetConditionFolder, ByValueSetConditionRegistry, ByValueSetConditionSoftware
Aliases: TaskSequence

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallationProperty
 

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases: InstallationProperties

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsAnyVersion
 

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

### -MsiFilePath
 

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

### -PackageId
 

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases: ClientPackageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreproductionPackageId
 

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases: PreproductionClientPackageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
 

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
Parameter Sets: ByIdSetConditionOperatingSystem, ByNameSetConditionOperatingSystem, ByValueSetConditionOperatingSystem
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
Parameter Sets: ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi, ByValueSetConditionQueryWmi
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
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
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
Parameter Sets: ByIdSetConditionSoftware, ByNameSetConditionSoftware, ByValueSetConditionSoftware
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

### -SupportedPlatform
 

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

