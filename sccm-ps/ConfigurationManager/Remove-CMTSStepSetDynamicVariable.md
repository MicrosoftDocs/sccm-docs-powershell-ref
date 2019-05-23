---
title: Remove-CMTSStepSetDynamicVariable
titleSuffix: Configuration Manager
description: Remove Set Dynamic Variable steps from a Configuration Manager task sequence.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Remove-CMTSStepSetDynamicVariable

## SYNOPSIS

Remove Set Dynamic Variable steps from a Configuration Manager task sequence.

## SYNTAX

### ByValue (Default)

```powershell
Remove-CMTSStepSetDynamicVariable [-InputObject] <IResultObject> [-StepName <String>] [-Force] [-WhatIf]
 [-Confirm]
```

### ById

```powershell
Remove-CMTSStepSetDynamicVariable [-TaskSequenceId] <String> [-StepName <String>] [-Force] [-WhatIf] [-Confirm]
```

### ByName

```powershell
Remove-CMTSStepSetDynamicVariable [-TaskSequenceName] <String> [-StepName <String>] [-Force] [-WhatIf]
 [-Confirm]
```

## DESCRIPTION

Remove task sequence â€œSet Dynamic Variableâ€ step(s) from a specific task sequence, it supports pipeline from a task sequence object, and could be filtered by the name of the step.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1

```powershell
PS XYZ:\> $ReferencedTaskSequence | Remove-CMTaskSequenceStepSetDynamicVariable -StepName $st1.Name -Force
```

This command removes a task sequence "Set Dynamic Variables" steps.

## PARAMETERS

### -Force

Forces the command to run without asking for user confirmation.

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

[New-CMTSStepSetDynamicVariable](./New-CMTSStepSetDynamicVariable.md)

[Get-CMTSStepSetDynamicVariable](./Get-CMTSStepSetDynamicVariable.md)

[Set-CMTSStepSetDynamicVariable](./Set-CMTSStepSetDynamicVariable.md)
