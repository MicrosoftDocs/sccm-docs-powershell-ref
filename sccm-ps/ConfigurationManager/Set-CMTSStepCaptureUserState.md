---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/12/2021
online version:
schema: 2.0.0
---

# Set-CMTSStepCaptureUserState

## SYNOPSIS

Configure an instance of the **Capture User State** task sequence step.

## SYNTAX

### ByValue (Default)
```
Set-CMTSStepCaptureUserState [-AddConfigFile <String[]>] [-CleanConfigFile] [-ConfigFile <String[]>]
 [-ContinueOnLockedFile <Boolean>] [-FileAccessOption <FileAccessType>] [-ModeOption <ModeType>]
 [-OfflineUserState <Boolean>] [-Package <IResultObject>] [-RemoveConfigFile <String[]>]
 [-SkipEncryptedFile <Boolean>] [-UseHardLinks <Boolean>] [-VerboseLogging <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>] -InputObject <IResultObject>
 [-IsContinueOnError <Boolean>] [-IsEnabled <Boolean>] [-MoveToIndex <Int32>] [-NewStepName <String>]
 [-RemoveConditionFile] [-RemoveConditionFolder] [-RemoveConditionIfStatement]
 [-RemoveConditionOperatingSystem] [-RemoveConditionQueryWmi] [-RemoveConditionRegistry]
 [-RemoveConditionSoftware] [-RemoveConditionVariable] [-StepName <String>] [-StepOrder <ReorderType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMTSStepCaptureUserState [-AddConfigFile <String[]>] [-CleanConfigFile] [-ConfigFile <String[]>]
 [-ContinueOnLockedFile <Boolean>] [-FileAccessOption <FileAccessType>] [-ModeOption <ModeType>]
 [-OfflineUserState <Boolean>] [-Package <IResultObject>] [-RemoveConfigFile <String[]>]
 [-SkipEncryptedFile <Boolean>] [-UseHardLinks <Boolean>] [-VerboseLogging <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-MoveToIndex <Int32>] [-NewStepName <String>] [-RemoveConditionFile]
 [-RemoveConditionFolder] [-RemoveConditionIfStatement] [-RemoveConditionOperatingSystem]
 [-RemoveConditionQueryWmi] [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-RemoveConditionVariable]
 [-StepName <String>] [-StepOrder <ReorderType>] -TaskSequenceId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMTSStepCaptureUserState [-AddConfigFile <String[]>] [-CleanConfigFile] [-ConfigFile <String[]>]
 [-ContinueOnLockedFile <Boolean>] [-FileAccessOption <FileAccessType>] [-ModeOption <ModeType>]
 [-OfflineUserState <Boolean>] [-Package <IResultObject>] [-RemoveConfigFile <String[]>]
 [-SkipEncryptedFile <Boolean>] [-UseHardLinks <Boolean>] [-VerboseLogging <Boolean>]
 [-AddCondition <IResultObject[]>] [-ClearCondition] [-Description <String>] [-IsContinueOnError <Boolean>]
 [-IsEnabled <Boolean>] [-MoveToIndex <Int32>] [-NewStepName <String>] [-RemoveConditionFile]
 [-RemoveConditionFolder] [-RemoveConditionIfStatement] [-RemoveConditionOperatingSystem]
 [-RemoveConditionQueryWmi] [-RemoveConditionRegistry] [-RemoveConditionSoftware] [-RemoveConditionVariable]
 [-StepName <String>] [-StepOrder <ReorderType>] -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionIfStatement
```
Set-CMTSStepCaptureUserState [-Condition <IResultObject[]>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionIfStatement
```
Set-CMTSStepCaptureUserState [-Condition <IResultObject[]>] [-SetConditionIfStatement]
 [-StatementType <ConditionStatementType>] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionIfStatement
```
Set-CMTSStepCaptureUserState [-Condition <IResultObject[]>] -InputObject <IResultObject>
 [-SetConditionIfStatement] [-StatementType <ConditionStatementType>] [-StepName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionVariable
```
Set-CMTSStepCaptureUserState [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-OperatorType <VariableOperatorType>] [-SetConditionVariable] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionVariable
```
Set-CMTSStepCaptureUserState [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 [-OperatorType <VariableOperatorType>] [-SetConditionVariable] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionVariable
```
Set-CMTSStepCaptureUserState [-ConditionVariableName <String>] [-ConditionVariableValue <String>]
 -InputObject <IResultObject> [-OperatorType <VariableOperatorType>] [-SetConditionVariable]
 [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByIdSetConditionFile
```
Set-CMTSStepCaptureUserState [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] [-SetConditionFile] [-StepName <String>]
 -TaskSequenceId <String> [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFile
```
Set-CMTSStepCaptureUserState [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] [-SetConditionFile] [-StepName <String>]
 -TaskSequenceName <String> [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFile
```
Set-CMTSStepCaptureUserState [-FileDateTimeOperator <VariableOperatorType>] [-FilePath <String>]
 [-FileTimestamp <DateTime>] [-FileVersion <String>] -InputObject <IResultObject> [-SetConditionFile]
 [-StepName <String>] [-VersionOperator <VariableOperatorType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionFolder
```
Set-CMTSStepCaptureUserState [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] [-SetConditionFolder] [-StepName <String>] -TaskSequenceId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionFolder
```
Set-CMTSStepCaptureUserState [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] [-SetConditionFolder] [-StepName <String>] -TaskSequenceName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionFolder
```
Set-CMTSStepCaptureUserState [-FolderDateTimeOperator <VariableOperatorType>] [-FolderPath <String>]
 [-FolderTimestamp <DateTime>] -InputObject <IResultObject> [-SetConditionFolder] [-StepName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionQueryWmi
```
Set-CMTSStepCaptureUserState -InputObject <IResultObject> [-Namespace <String[]>] [-Query <String>]
 [-SetConditionQueryWmi] [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionOperatingSystem
```
Set-CMTSStepCaptureUserState -InputObject <IResultObject> [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionRegistry
```
Set-CMTSStepCaptureUserState -InputObject <IResultObject> [-RegistryKey <String>]
 [-RegistryOperator <VariableOperatorType>] [-RegistryValueData <String>] [-RegistryValueName <String>]
 [-RootKey <RegistryRootKeyType>] [-SetConditionRegistry] [-StepName <String>] [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueSetConditionSoftware
```
Set-CMTSStepCaptureUserState -InputObject <IResultObject> [-IsAnyVersion <Boolean>] [-MsiFilePath <String>]
 [-SetConditionSoftware] [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionSoftware
```
Set-CMTSStepCaptureUserState [-IsAnyVersion <Boolean>] [-MsiFilePath <String>] [-SetConditionSoftware]
 [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionSoftware
```
Set-CMTSStepCaptureUserState [-IsAnyVersion <Boolean>] [-MsiFilePath <String>] [-SetConditionSoftware]
 [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionQueryWmi
```
Set-CMTSStepCaptureUserState [-Namespace <String[]>] [-Query <String>] [-SetConditionQueryWmi]
 [-StepName <String>] -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionQueryWmi
```
Set-CMTSStepCaptureUserState [-Namespace <String[]>] [-Query <String>] [-SetConditionQueryWmi]
 [-StepName <String>] -TaskSequenceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionRegistry
```
Set-CMTSStepCaptureUserState [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueData <String>] [-RegistryValueName <String>] [-RootKey <RegistryRootKeyType>]
 [-SetConditionRegistry] [-StepName <String>] -TaskSequenceId <String> [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionRegistry
```
Set-CMTSStepCaptureUserState [-RegistryKey <String>] [-RegistryOperator <VariableOperatorType>]
 [-RegistryValueData <String>] [-RegistryValueName <String>] [-RootKey <RegistryRootKeyType>]
 [-SetConditionRegistry] [-StepName <String>] -TaskSequenceName <String> [-ValueType <RegistryValueType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdSetConditionOperatingSystem
```
Set-CMTSStepCaptureUserState [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] -TaskSequenceId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameSetConditionOperatingSystem
```
Set-CMTSStepCaptureUserState [-SetConditionOperatingSystem] [-StepName <String>]
 [-SupportedPlatform <IResultObject[]>] -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure an instance of the **Capture User State** task sequence step.

For more information on this step, see [About task sequence steps: Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example changes the **Capture User State** step in the **Default OS deployment** task sequence to use custom capture with a configuration file.

```powershell
$tsNameOsd = "Default OS deployment"
$tsStepNameCapState = "Capture User State"

Set-CMTSStepCaptureUserState -TaskSequenceName $tsNameOsd -StepName $tsStepNameCapState -ModeOption Customize -ConfigFiles "contoso.xml"
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

### -AddConfigFile

When you specify `-ModeOption Customize` to customize how user profiles are captured, use this parameter to add file names of custom XML configuration files. These files need to be in the USMT package. Use this parameter to append to an existing list. To create a new list, use the **ConfigFile** parameter.

```yaml
Type: String[]
Parameter Sets: ByValue, ById, ByName
Aliases: AddConfigFiles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanConfigFile

Add this parameter to remove all of the file names for custom XML configuration files. To remove individual file names, use the **RemoveConfigFile** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: ByValue, ById, ByName
Aliases: CleanConfigFiles

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

### -ConfigFile

When you specify `-ModeOption Customize` to customize how user profiles are captured, use this parameter to specify the file names of custom XML configuration files. These files need to be in the USMT package. Use this parameter to create a new list. To append to an existing list, use the **AddConfigFile** parameter.

```yaml
Type: String[]
Parameter Sets: ByValue, ById, ByName
Aliases: ConfigFiles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinueOnLockedFile

When you specify `-FileAccessOption Normal`, set this parameter to `$true` to allow USMT to continue if some files can't be captured.

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

### -FileAccessOption

There are two options for how USMT accesses the file system:

- `Normal`: USMT uses standard file system access. When you specify this option, you can also enable **ContinueOnLockedFile**, **OfflineUserState**, and **-**.

- `VolumeCopyShadowService`: USMT uses the Volume Copy Shadow Services (VSS).

```yaml
Type: FileAccessType
Parameter Sets: ByValue, ById, ByName
Aliases:
Accepted values: Normal, VolumeCopyShadowService

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

Specify a task sequence object from which to get the **Capture User State** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

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

### -ModeOption

There are two modes in which USMT can operate:

- `Standard`: Capture all user profiles by using standard options. This option is the default.

- `Customize`: Customize how user profiles are captured. If you specify this option, use the **ConfigFile** parameter to specify the custom XML configuration files.

```yaml
Type: ModeType
Parameter Sets: ByValue, ById, ByName
Aliases:
Accepted values: Standard, Customize

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

### -OfflineUserState

When you specify `-FileAccessOption Normal`, set this parameter to `$true` to capture in offline mode in Windows PE.

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

### -Package

Specify an object for the USMT package. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue, ById, ByName
Aliases: UserStateMigrationToolPackage

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

### -RemoveConfigFile

Specify the file names of custom XML configuration files to remove from the list. To remove all configuration files, use the **CleanConfigFile** parameter.

```yaml
Type: String[]
Parameter Sets: ByValue, ById, ByName
Aliases: RemoveConfigFiles

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

### -SkipEncryptedFile

Set this parameter to `$true` to skip files that use the encrypting file system (EFS).

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

Specify the **package ID** of the task sequence from which to get the **Capture User State** step. This value is a standard package ID, for example `XYZ00858`.

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

### -UseHardLinks

When you specify `-FileAccessOption Normal`, set this parameter to `$true` to capture locally by using NTFS hard-links.

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

### -VerboseLogging

Set this parameter to `$true` to enable USMT verbose logging.

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

[Get-CMTSStepCaptureUserState](Get-CMTSStepCaptureUserState.md)
[New-CMTSStepCaptureUserState](New-CMTSStepCaptureUserState.md)
[Remove-CMTSStepCaptureUserState](Remove-CMTSStepCaptureUserState.md)

[About task sequence steps: Capture User State](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureUserState)
