---
title: 
titleSuffix: Configuration Manager
description: 
ms.date: 11/29/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Remove-CMTSStepSetDynamicVariable

## SYNOPSIS

{{Fill in the Synopsis}}

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

{{Fill in the Description}}

## EXAMPLES

### Example 1

```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -Force

{{Fill Force Description}}

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
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -TaskSequenceId

{{Fill TaskSequenceId Description}}

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

{{Fill TaskSequenceName Description}}

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

## NOTES

## RELATED LINKS

* [New-CMTSStepSetDynamicVariable](./New-CMTSStepSetDynamicVariable.md)
* [Get-CMTSStepSetDynamicVariable](./Get-CMTSStepSetDynamicVariable.md)
* [Set-CMTSStepSetDynamicVariable](./Set-CMTSStepSetDynamicVariable.md)
