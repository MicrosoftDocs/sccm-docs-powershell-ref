---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/01/2021
online version:
schema: 2.0.0
---

# Set-CMTSStepSetVariable

## SYNOPSIS

Configure an instance of the **Set Task Sequence Variable** task sequence step.

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-TaskSequenceVariable <String>]
 [-TaskSequenceVariableValue <String>] [-AddCondition <IResultObject[]>] [-ClearCondition]
 [-Description <String>] -InputObject <IResultObject> [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>]
 [-MoveToIndex <Int32>] [-NewStepName <String>] [-RemoveConditionFile] [-RemoveConditionFolder]
 [-RemoveConditionIfStatement] [-RemoveConditionOperatingSystem] [-RemoveConditionQueryWmi]
 [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-RemoveConditionVariable] [-StepName <String>]
 [-StepOrder <ReorderType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-TaskSequenceVariable <String>]
 [-TaskSequenceVariableValue <String>] [-AddCondition <IResultObject[]>] [-ClearCondition]
 [-Description <String>] [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-MoveToIndex <Int32>]
 [-NewStepName <String>] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionIfStatement]
 [-RemoveConditionOperatingSystem] [-RemoveConditionQueryWmi] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-RemoveConditionVariable] [-StepName <String>] [-StepOrder <ReorderType>]
 -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-TaskSequenceVariable <String>]
 [-TaskSequenceVariableValue <String>] [-AddCondition <IResultObject[]>] [-ClearCondition]
 [-Description <String>] [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-MoveToIndex <Int32>]
 [-NewStepName <String>] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionIfStatement]
 [-RemoveConditionOperatingSystem] [-RemoveConditionQueryWmi] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-RemoveConditionVariable] [-StepName <String>] [-StepOrder <ReorderType>]
 -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-Condition <IResultObject[]>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-Condition <IResultObject[]>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-Condition <IResultObject[]>] -InputObject <IResultObject>
 [-SetConditionIfStatement] [-StatementType <ConditionStatementType>] [-StepName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-ConditionVariableName <String>]
 [-ConditionVariableValue <String>] [-OperatorType <VariableOperatorType>] [-SetConditionVariable]
 [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-ConditionVariableName <String>]
 [-ConditionVariableValue <String>] [-OperatorType <VariableOperatorType>] [-SetConditionVariable]
 [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-ConditionVariableName <String>]
 [-ConditionVariableValue <String>] -InputObject <IResultObject> [-OperatorType <VariableOperatorType>]
 [-SetConditionVariable] [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-FileDateTimeOperator <VariableOperatorType>]
 [-FilePath <String>] [-FileTimestamp <DateTime>] [-FileVersion <String>] [-SetConditionFile]
 [-StepName <String>] -TaskSequenceId <String> [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-FileDateTimeOperator <VariableOperatorType>]
 [-FilePath <String>] [-FileTimestamp <DateTime>] [-FileVersion <String>] [-SetConditionFile]
 [-StepName <String>] -TaskSequenceName <String> [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-FileDateTimeOperator <VariableOperatorType>]
 [-FilePath <String>] [-FileTimestamp <DateTime>] [-FileVersion <String>] -InputObject <IResultObject>
 [-SetConditionFile] [-StepName <String>] [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-SetConditionFolder] [-StepName <String>]
 -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-SetConditionFolder] [-StepName <String>]
 -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] -InputObject <IResultObject> [-SetConditionFolder]
 [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] -InputObject <IResultObject> [-Namespace <String[]>]
 [-Query <String>] [-SetConditionQueryWmi] [-StepName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] -InputObject <IResultObject> [-SetConditionOperatingSystem]
 [-StepName <String>] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] -InputObject <IResultObject> [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueData <String>] [-RegistryValueName <String>]
 [-RootKey <RegistryRootKeyType>] [-SetConditionRegistry] [-StepName <String>] [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] -InputObject <IResultObject> [-IsAnyVersion <Boolean>]
 [-MsiFilePath <String>] [-SetConditionSoftware] [-StepName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-IsAnyVersion <Boolean>] [-MsiFilePath <String>]
 [-SetConditionSoftware] [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-IsAnyVersion <Boolean>] [-MsiFilePath <String>]
 [-SetConditionSoftware] [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-Namespace <String[]>] [-Query <String>] [-SetConditionQueryWmi]
 [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-Namespace <String[]>] [-Query <String>] [-SetConditionQueryWmi]
 [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueData <String>] [-RegistryValueName <String>]
 [-RootKey <RegistryRootKeyType>] [-SetConditionRegistry] [-StepName <String>] -TaskSequenceId <String>
 [-ValueType <RegistryValueType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueData <String>] [-RegistryValueName <String>]
 [-RootKey <RegistryRootKeyType>] [-SetConditionRegistry] [-StepName <String>] -TaskSequenceName <String>
 [-ValueType <RegistryValueType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] -TaskSequenceId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepSetVariable [-IsMasked <Boolean>] [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure an instance of the **Set Task Sequence Variable** task sequence step.

For more information on this step, see [About task sequence steps: Set Task Sequence Variable](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetTaskSequenceVariable).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **ConvertTo-SecureString** built-in cmdlet to create a secure string for the user password. This method is used here as a simple example, but not the most secure since the plain text password is in the script. For more information on this cmdlet and other options, see [ConvertTo-SecureString](/powershell/module/microsoft.powershell.security/convertto-securestring).

It then changes the **Set Task Sequence Variable** step in the **Default OS deployment** task sequence to use this new password, and mask the variable value.

```powershell
$Secure_String_Pwd = ConvertTo-SecureString "P@ssW0rD!" -AsPlainText -Force

$tsNameOsd = "Default OS deployment"
$tsStepNameSetTSVar = "Set Task Sequence Variable"

Set-CMTSStepSetVariable -TaskSequenceName $tsNameOsd -StepName $tsStepNameSetTSVar -TaskSequenceVariable "OSDJoinPassword" -TaskSequenceVariableValue $Secure_String_Pwd -IsMasked $true -Description "Password updated $(Get-Date)"
```

## PARAMETERS

### -AddCondition

Specify a condition object to add to this step. To get this object, use one of the task sequence condition cmdlets. For example, [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md).

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

Remove a condition from this step. Use the **-Condition** parameter to specify the condition to remove.

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

Specify a condition object to use with this step. To get this object, use one of the task sequence condition cmdlets. For example, [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md).

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

Specify the name of the task sequence variable to use as a condition.

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

Specify the value of the task sequence variable to use in a condition.

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

Specify an optional description for this task sequence step.

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

Specify a variable operator type for a file date/time condition.

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

Specify the path for a file condition.

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

Specify a date/time value to use for a file condition.

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

Specify a version string for a file condition.

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

Specify a variable operator for a folder date/time condition.

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

Specify the path for a folder condition.

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

Specify a date/time value to use for a folder condition.

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

### -InputObject

Specify a task sequence object from which to get the **Set Task Sequence Variable** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

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

Use this parameter with the **SetConditionSoftware** parameter to match any version of the product.

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

Use this parameter to enable the step option **Continue on error**. When you enable this option, if the step fails, the task sequence continues.

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

Use this parameter to enable this task sequence step.

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

### -IsMasked

Set this parameter to `$true` to mask sensitive data stored in task sequence variables. For example, when specifying a password.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: IsHidden, IsMask

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

Specify the path to a Windows Installer file for a software condition.

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

Specify the namespace for a WMI query condition.

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

Use this parameter to rename this task sequence step.

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

Specify an operator to use with a task sequence variable condition.

```yaml
Type: VariableOperatorType
Parameter Sets: ByIdSetConditionVariable, ByNameSetConditionVariable, ByValueSetConditionVariable
Aliases:
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual, Like, NotLike

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query

Specify a WMI query string to use for a condition.

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

Specify the key to use with a registry condition.

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

Specify an operator to use with a registry condition.

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

Specify the value data to use with a registry condition.

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

Specify the value name to use with a registry condition.

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

Use this parameter to remove a file condition.

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

Use this parameter to remove a folder condition.

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

Use this parameter to remove an `if` statement condition.

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

Use this parameter to remove an OS condition.

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

Use this parameter to remove a WMI query condition.

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

Use this parameter to remove a registry condition.

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

Use this parameter to remove a software condition.

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

Use this parameter to remove a task sequence variable condition.

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

Specify the root key to use with a registry condition.

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

Add a new file condition.

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

Add a new folder condition.

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

Add a new `if` statement condition.

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

Add a new OS condition.

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

Add a new WMI query condition.

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

Add a new registry condition.

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

Add a new software condition.

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

Add a new task sequence variable condition.

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

Set the type for an `if` statement condition.

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

Specify the name of the step to select for changes.

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

Use this parameter to specify the platforms for an OS condition.

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

Specify the **package ID** of the task sequence from which to get the **Set Task Sequence Variable** step. This value is a standard package ID, for example `XYZ00858`.

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

Specify the name of the task sequence to target for changes.

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

### -TaskSequenceVariable

Specify the name of a task sequence built-in or action variable, or specify your own user-defined variable name. For more information, see [How to use task sequence variables in Configuration Manager](/mem/configmgr/osd/understand/using-task-sequence-variables) and the reference of [Task sequence variables](/mem/configmgr/osd/understand/task-sequence-variables).

Use the **TaskSequenceVariableValue** parameter to set the value.

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases: VariableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceVariableValue

The task sequence sets the **TaskSequenceVariable** to this value. Set this task sequence variable to the value of another task sequence variable with the syntax `%varname%`.

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases: VariableValue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueType

Specify the type of value for a registry condition.

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

Specify an operator to use with a file condition.

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

[Get-CMTSStepSetVariable](Get-CMTSStepSetVariable.md)
[New-CMTSStepSetVariable](New-CMTSStepSetVariable.md)
[Remove-CMTSStepSetVariable](Remove-CMTSStepSetVariable.md)

[About task sequence steps: Set Task Sequence Variable](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetTaskSequenceVariable)
