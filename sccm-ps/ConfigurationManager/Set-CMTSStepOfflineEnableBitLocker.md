---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2021
online version:
schema: 2.0.0
---

# Set-CMTSStepOfflineEnableBitLocker

## SYNOPSIS

Configure an instance of the **Pre-provision BitLocker** task sequence step.

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepOfflineEnableBitLocker [-Disk <Int32>] [-Drive <String>] [-EnableSkipWhenTpmInvalid <Boolean>]
 [-EncryptionMethod <DiskEncryptionMethod>] [-NextPartition] [-Partition <Int32>] [-VariableName <String>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>] -InputObject <IResultObject>
 [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-MoveToIndex <Int32>] [-NewStepName <String>]
 [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionIfStatement]
 [-RemoveConditionOperatingSystem] [-RemoveConditionQueryWmi] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-RemoveConditionVariable] [-StepName <String>] [-StepOrder <ReorderType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMTSStepOfflineEnableBitLocker [-Disk <Int32>] [-Drive <String>] [-EnableSkipWhenTpmInvalid <Boolean>]
 [-EncryptionMethod <DiskEncryptionMethod>] [-NextPartition] [-Partition <Int32>] [-VariableName <String>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-MoveToIndex <Int32>] [-NewStepName <String>] [-RemoveConditionFile]
 [-RemoveConditionFolder] [-RemoveConditionIfStatement] [-RemoveConditionOperatingSystem]
 [-RemoveConditionQueryWmi] [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-RemoveConditionVariable]
 [-StepName <String>] [-StepOrder <ReorderType>] -TaskSequenceId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMTSStepOfflineEnableBitLocker [-Disk <Int32>] [-Drive <String>] [-EnableSkipWhenTpmInvalid <Boolean>]
 [-EncryptionMethod <DiskEncryptionMethod>] [-NextPartition] [-Partition <Int32>] [-VariableName <String>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-MoveToIndex <Int32>] [-NewStepName <String>] [-RemoveConditionFile]
 [-RemoveConditionFolder] [-RemoveConditionIfStatement] [-RemoveConditionOperatingSystem]
 [-RemoveConditionQueryWmi] [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-RemoveConditionVariable]
 [-StepName <String>] [-StepOrder <ReorderType>] -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepOfflineEnableBitLocker [-Condition <IResultObject[]>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepOfflineEnableBitLocker [-Condition <IResultObject[]>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepOfflineEnableBitLocker [-Condition <IResultObject[]>] -InputObject <IResultObject>
 [-SetConditionIfStatement] [-StatementType <ConditionStatementType>] [-StepName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepOfflineEnableBitLocker [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-OperatorType <VariableOperatorType>] [-SetConditionVariable] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepOfflineEnableBitLocker [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-OperatorType <VariableOperatorType>] [-SetConditionVariable] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepOfflineEnableBitLocker [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 -InputObject <IResultObject> [-OperatorType <VariableOperatorType>] [-SetConditionVariable]
 [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepOfflineEnableBitLocker [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] [-SetConditionFile] [-StepName <String>]
 -TaskSequenceId <String> [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepOfflineEnableBitLocker [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] [-SetConditionFile] [-StepName <String>]
 -TaskSequenceName <String> [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepOfflineEnableBitLocker [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] -InputObject <IResultObject> [-SetConditionFile]
 [-StepName <String>] [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepOfflineEnableBitLocker [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] [-SetConditionFolder] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepOfflineEnableBitLocker [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] [-SetConditionFolder] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepOfflineEnableBitLocker [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] -InputObject <IResultObject> [-SetConditionFolder] [-StepName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepOfflineEnableBitLocker -InputObject <IResultObject> [-Namespace <String[]>] [-Query <String>]
 [-SetConditionQueryWmi] [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepOfflineEnableBitLocker -InputObject <IResultObject> [-SetConditionOperatingSystem]
 [-StepName <String>] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepOfflineEnableBitLocker -InputObject <IResultObject> [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueData <String>] [-RegistryValueName <String>]
 [-RootKey <RegistryRootKeyType>] [-SetConditionRegistry] [-StepName <String>] [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepOfflineEnableBitLocker -InputObject <IResultObject> [-IsAnyVersion <Boolean>]
 [-MsiFilePath <String>] [-SetConditionSoftware] [-StepName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepOfflineEnableBitLocker [-IsAnyVersion <Boolean>] [-MsiFilePath <String>] [-SetConditionSoftware]
 [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepOfflineEnableBitLocker [-IsAnyVersion <Boolean>] [-MsiFilePath <String>] [-SetConditionSoftware]
 [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepOfflineEnableBitLocker [-Namespace <String[]>] [-Query <String>] [-SetConditionQueryWmi]
 [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepOfflineEnableBitLocker [-Namespace <String[]>] [-Query <String>] [-SetConditionQueryWmi]
 [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepOfflineEnableBitLocker [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueData <String>] [-RegistryValueName <String>] [-RootKey <RegistryRootKeyType>]
 [-SetConditionRegistry] [-StepName <String>] -TaskSequenceId <String> [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepOfflineEnableBitLocker [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueData <String>] [-RegistryValueName <String>] [-RootKey <RegistryRootKeyType>]
 [-SetConditionRegistry] [-StepName <String>] -TaskSequenceName <String> [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepOfflineEnableBitLocker [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] -TaskSequenceId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepOfflineEnableBitLocker [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure an instance of the **Pre-provision BitLocker** task sequence step.

For more information on this step, see [About task sequence steps: Pre-provision BitLocker](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_PreProvisionBitLocker).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example changes the **Pre-provision BitLocker** step in the **Default OS deployment** task sequence to use specific disk and partition numbers, and save the logical drive letter as a variable.

```powershell
$tsNameOsd = "Default OS deployment"
$tsStepNamePreProvBitLocker = "Pre-provision BitLocker"

Set-CMTSStepOfflineEnableBitLocker -TaskSequenceName $tsNameOsd -StepName $tsStepNamePreProvBitLocker -Disk 1 -Partition 2 -VariableName "BitLockerDrive"
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

### -Disk

Specify the specific disk number to encrypt. Use this parameter with the **-Partition** parameter.

```yaml
Type: Int32
Parameter Sets: ByValue, ById, ByName
Aliases: DestinationDisk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Drive

Specify the logical drive letter to encrypt. For example, `C:`

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases: SpecificDrive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSkipWhenTpmInvalid

Set this parameter to `true` to skip this step for computers that don't have a TPM or when the TPM isn't enabled.

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

### -EncryptionMethod

Applies to version 2006 and later. Use this parameter to specify the disk encryption mode. By default or if not specified, the step continues to use the default encryption method for the OS version.

```yaml
Type: DiskEncryptionMethod
Parameter Sets: ByValue, ById, ByName
Aliases: DiskEncryptionMethod
Accepted values: DoNotSpecify, AES_128, AES_256, XTS_AES128, XTS_AES256, TotalCount

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

Specify a task sequence object from which to get the **Pre-provision BitLocker** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

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

### -NextPartition

Add this parameter to configure BitLocker to apply to the next available formatted partition.

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases: UseNextAvailableFormattedPartition

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

### -Partition

Specify the specific partition number to encrypt. Use this parameter with the **-Disk** parameter.

```yaml
Type: Int32
Parameter Sets: ByValue, ById, ByName
Aliases: DestinationPartition

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
Specify the ID of the task sequence to target for changes.

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

### -VariableName

Specify a task sequence variable to identify the logical drive letter as the destination for BitLocker.

```yaml
Type: String
Parameter Sets: ByValue, ById, ByName
Aliases: DestinationVariable

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

[Get-CMTSStepOfflineEnableBitLocker](Get-CMTSStepOfflineEnableBitLocker.md)
[New-CMTSStepOfflineEnableBitLocker](New-CMTSStepOfflineEnableBitLocker.md)
[Remove-CMTSStepOfflineEnableBitLocker](Remove-CMTSStepOfflineEnableBitLocker.md)

[About task sequence steps: Pre-provision BitLocker](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_PreProvisionBitLocker)
