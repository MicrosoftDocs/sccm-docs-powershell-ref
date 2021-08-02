---
description: Gets task sequence Set Dynamic Variable steps in Configuration Manager.
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 01/08/2019
schema: 2.0.0
title: Get-CMTSStepSetDynamicVariable
---

# Get-CMTSStepSetDynamicVariable

## SYNOPSIS

Gets task sequence Set Dynamic Variable steps in Configuration Manager.

## SYNTAX

### ByValue (Default)
```
Get-CMTSStepSetDynamicVariable [-InputObject] <IResultObject> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Get-CMTSStepSetDynamicVariable [-TaskSequenceId] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Get-CMTSStepSetDynamicVariable [-TaskSequenceName] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMTSStepSetDynamicVariable** gets task sequence "Set Dynamic Variable" step(s) in a task sequence. This command supports pipeline from a task sequence object, and could be filtered by the name of the step.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> $ReferencedTaskSequence | Get-CMTaskSequenceStepSetDynamicVariable -StepName $stepName
```

This command gets task sequence "Set Dynamic Variable" steps in a task sequence.

## PARAMETERS

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
## NOTES

## RELATED LINKS

[New-CMTSStepSetDynamicVariable](./New-CMTSStepSetDynamicVariable.md)

[Set-CMTSStepSetDynamicVariable](./Set-CMTSStepSetDynamicVariable.md)

[Remove-CMTSStepSetDynamicVariable](./Remove-CMTSStepSetDynamicVariable.md)
