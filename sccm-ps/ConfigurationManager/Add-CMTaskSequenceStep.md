---
title: Add-CMTaskSequenceStep
titleSuffix: Configuration Manager
description: Adds a Configuration Manager task sequence step.
ms.date: 11/30/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Add-CMTaskSequenceStep

## SYNOPSIS

Adds a Configuration Manager task sequence step.

## SYNTAX

### ByValue (Default)

```powershell
Add-CMTaskSequenceStep -Step <IResultObject[]> [-InsertStepStartIndex <UInt32>] -InputObject <IResultObject>
 [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById

```powershell
Add-CMTaskSequenceStep -Step <IResultObject[]> [-InsertStepStartIndex <UInt32>] -TaskSequenceId <String>
 [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName

```powershell
Add-CMTaskSequenceStep -Step <IResultObject[]> [-InsertStepStartIndex <UInt32>] -TaskSequenceName <String>
 [-StepName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMTaskSequenceStep** cmdlet adds task sequence group or step object(s) to a specific task sequence. The cmdlet supports pipeline from a task sequence object, and can be filtered by the name of the group/step.

## EXAMPLES

### Example 1

```powershell
PS C:\>$ReferencedTaskSequence | Add-CMTaskSequenceStep -Step ($gp1,$st1,$st2)
```

This command adds a task sequence group and two task sequence steps to a task sequence.

### Example 2

```powershell
PS C:\>$ReferencedTaskSequence | Add-CMTaskSequenceStep -Step $st3 -InsertStepStartIndex $index
```

This command adds a step to a task sequence with a start index.

## PARAMETERS

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

Specifies a task sequence object. 

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InsertStepStartIndex

Specifies the inserted steps start index.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: InsertStepsStartIndex

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Step

Specifies the step objects.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Steps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StepName

Specifies the name of a step.

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

Specifies the ID of a task sequence.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id, TaskSequencePackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specifies the name of a task sequence.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
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

## RELATED LINKS

- [Get-CMTaskSequenceStep](./Get-CMTaskSequenceStep.md)
- [Get-CMTaskSequenceStepCondition](./Get-CMTaskSequenceStepCondition.md)
- [Remove-CMTaskSequenceStep](./Remove-CMTaskSequenceStep.md)
- [Get-CMTaskSequenceGroup](./Get-CMTaskSequenceGroup.md)
