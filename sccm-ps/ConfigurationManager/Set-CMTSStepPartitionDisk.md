---
description: Configure the Format and Partition Disk step in a task sequence.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/29/2020
schema: 2.0.0
title: Set-CMTSStepPartitionDisk
---

# Set-CMTSStepPartitionDisk

## SYNOPSIS

Configure the **Format and Partition Disk** step in a task sequence.

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepPartitionDisk [-DiskType <PartitionDiskStyle>] [-IsBootDisk <Boolean>] [-DiskNumber <Int32>]
 [-DiskNumberVariable <String>] [-PartitionSetting <IResultObject[]>] -InputObject <IResultObject>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>]
 [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Set-CMTSStepPartitionDisk [-DiskType <PartitionDiskStyle>] [-IsBootDisk <Boolean>] [-DiskNumber <Int32>]
 [-DiskNumberVariable <String>] [-PartitionSetting <IResultObject[]>] -TaskSequenceId <String>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>]
 [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Set-CMTSStepPartitionDisk [-DiskType <PartitionDiskStyle>] [-IsBootDisk <Boolean>] [-DiskNumber <Int32>]
 [-DiskNumberVariable <String>] [-PartitionSetting <IResultObject[]>] -TaskSequenceName <String>
 [-StepName <String>] [-NewStepName <String>] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-AddCondition <IResultObject[]>] [-ClearCondition] [-StepOrder <ReorderType>]
 [-MoveToIndex <Int32>] [-RemoveConditionIfStatement] [-RemoveConditionQueryWmi] [-RemoveConditionVariable]
 [-RemoveConditionOperatingSystem] [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepPartitionDisk -TaskSequenceId <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepPartitionDisk -TaskSequenceId <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepPartitionDisk -TaskSequenceId <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepPartitionDisk -TaskSequenceId <String> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepPartitionDisk -TaskSequenceId <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepPartitionDisk -TaskSequenceId <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepPartitionDisk -TaskSequenceId <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepPartitionDisk -TaskSequenceId <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepPartitionDisk -TaskSequenceName <String> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepPartitionDisk -TaskSequenceName <String> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepPartitionDisk -TaskSequenceName <String> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepPartitionDisk -TaskSequenceName <String> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepPartitionDisk -TaskSequenceName <String> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepPartitionDisk -TaskSequenceName <String> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepPartitionDisk -TaskSequenceName <String> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepPartitionDisk -TaskSequenceName <String> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepPartitionDisk -InputObject <IResultObject> [-StepName <String>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepPartitionDisk -InputObject <IResultObject> [-StepName <String>] [-SetConditionQueryWmi]
 [-Namespace <String[]>] [-Query <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepPartitionDisk -InputObject <IResultObject> [-StepName <String>] [-SetConditionVariable]
 [-OperatorType <VariableOperatorType>] [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepPartitionDisk -InputObject <IResultObject> [-StepName <String>] [-SetConditionOperatingSystem]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepPartitionDisk -InputObject <IResultObject> [-StepName <String>] [-SetConditionFile]
 [-FilePath <String>] [-FileVersion <String>] [-FileTimestamp <DateTime>]
 [-FileDateTimeOperator <VariableOperatorType>] [-VersionOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepPartitionDisk -InputObject <IResultObject> [-StepName <String>] [-SetConditionFolder]
 [-FolderPath <String>] [-FolderTimestamp <DateTime>] [-FolderDateTimeOperator <VariableOperatorType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepPartitionDisk -InputObject <IResultObject> [-StepName <String>] [-SetConditionRegistry]
 [-RootKey <RegistryRootKeyType>] [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueName <String>] [-ValueType <RegistryValueType>] [-RegistryValueData <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepPartitionDisk -InputObject <IResultObject> [-StepName <String>] [-SetConditionSoftware]
 [-MsiFilePath <String>] [-IsAnyVersion <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Configure the **Format and Partition Disk** step in a task sequence. For more information on this task sequence step, see [About task sequence steps](https://docs.microsoft.com/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

{{ Add example description here }}

```powershell
{{ Add example code here }}
```

## PARAMETERS

### -AddCondition

Specify a condition object to add to this step.

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

Specify a condition object to use with this step.

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

### -DiskNumber

Specify an integer for the physical disk number of the disk to format. The number is based on Windows disk enumeration ordering.

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

### -DiskNumberVariable

Applies to version 2006 and later. Use a task sequence variable to specify the target disk to format. This variable option supports more complex task sequences with dynamic behaviors. For more information, see [About task sequence steps - Format and Parition Disk](https://docs.microsoft.com/mem/configmgr/osd/understand/task-sequence-steps#properties-for-format-and-partition-disk).

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

### -DiskType

Specify the type of the disk to format:

- `Mbr`: Master Boot Record
- `Gpt`: GUID Partition Table

```yaml
Type: PartitionDiskStyle
Parameter Sets: ByValue, ById, ByName
Aliases:
Accepted values: Mbr, Gpt

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

Specify a variable operator type for a folder date/time condition.

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

### -IsBootDisk

For a new partition, set this parameter to `true` to make it the boot partition.

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

Specify the path to a Windows Installer file for an software condition.

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

Specify the namespace for a WMI query condition.

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
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual, Like

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionSetting

Specify an array of partition setting objects.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue, ById, ByName
Aliases: PartitionSettings

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
Parameter Sets: ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi, ByValueSetConditionQueryWmi
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
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
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

Specify the value data to use with a registry condition.

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
Specify the value name to use with a registry condition.

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
Parameter Sets: ByIdSetConditionOperatingSystem, ByNameSetConditionOperatingSystem, ByValueSetConditionOperatingSystem
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
Parameter Sets: ByIdSetConditionQueryWmi, ByNameSetConditionQueryWmi, ByValueSetConditionQueryWmi
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
Parameter Sets: ByIdSetConditionRegistry, ByNameSetConditionRegistry, ByValueSetConditionRegistry
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
Parameter Sets: ByIdSetConditionSoftware, ByNameSetConditionSoftware, ByValueSetConditionSoftware
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
Parameter Sets: ByIdSetConditionOperatingSystem, ByNameSetConditionOperatingSystem, ByValueSetConditionOperatingSystem
Aliases: SupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceId
Specify the ID of the task sequence to target for changes.

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
Specify the name of the task sequence to target for changes.

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
Specify the type of value for a registry condition.

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

Shows what would happen if the cmdlet runs. It doesn't run the cmdlet.

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

[About task sequence steps - Format and Partition Disk](https://docs.microsoft.com/mem/configmgr/osd/understand/task-sequence-steps#BKMK_FormatandPartitionDisk)
