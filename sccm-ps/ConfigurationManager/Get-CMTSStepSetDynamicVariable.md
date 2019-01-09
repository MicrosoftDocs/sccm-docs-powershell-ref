---
title: Get-CMTSStepSetDynamicVariable
titleSuffix: Configuration Manager
description: Gets task sequence Set Dynamic Variable steps in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Get-CMTSStepSetDynamicVariable

## SYNOPSIS

Gets task sequence Set Dynamic Variable steps in Configuration Manager.

## SYNTAX

### ByValue (Default)

```powershell
Get-CMTSStepSetDynamicVariable [-InputObject] <IResultObject> [-StepName <String>] [-WhatIf] [-Confirm]
```

### ById

```powershell
Get-CMTSStepSetDynamicVariable [-TaskSequenceId] <String> [-StepName <String>] [-WhatIf] [-Confirm]
```

### ByName

```powershell
Get-CMTSStepSetDynamicVariable [-TaskSequenceName] <String> [-StepName <String>] [-WhatIf] [-Confirm]
```

## DESCRIPTION

The **Get-CMTSStepSetDynamicVariable** gets task sequence "Set Dynamic Variable" step(s) in a task sequence. This command supports pipeline from a task sequence object, and could be filtered by the name of the step.

## EXAMPLES

### Example 1

```powershell
PS C:\> $ReferencedTaskSequence | Get-CMTaskSequenceStepSetDynamicVariable -StepName $stepName
```

This command gets task sequence "Set Dynamic Variable" steps in a task sequence. 

## PARAMETERS

### -InputObject

Specifies a task sequence object.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StepName

Specifies a name for the step.

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

### -TaskSequenceId

Specifies a task sequence ID.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id, TaskSequencePackageId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specifies a task sequence name.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
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

* [New-CMTSStepSetDynamicVariable](./New-CMTSStepSetDynamicVariable.md)
* [Set-CMTSStepSetDynamicVariable](./Set-CMTSStepSetDynamicVariable.md)
* [Remove-CMTSStepSetDynamicVariable](./Remove-CMTSStepSetDynamicVariable.md)