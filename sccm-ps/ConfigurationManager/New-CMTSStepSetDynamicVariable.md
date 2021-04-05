---
description: Create a task sequence Set Dynamic Variable step in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/08/2019
schema: 2.0.0
title: New-CMTSStepSetDynamicVariable
---

# New-CMTSStepSetDynamicVariable

## SYNOPSIS

Create a task sequence Set Dynamic Variable step in Configuration Manager.

## SYNTAX

```
New-CMTSStepSetDynamicVariable -AddRule <IResultObject[]> [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMTSStepSetDynamicVariable** creates a task sequence "Set Dynamic Variable" step object with specific name, description, specific properties, options and conditions, which could be used by [Add-CMTaskSequenceStep](./Add-CMTaskSequenceStep.md) and [Set-CMTaskSequenceGroup](./Set-CMTaskSequenceGroup.md).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> Add-CMTaskSequenceStep -TaskSequenceName $TSName | New-CMTaskSequenceStepSetDynamicVariable -Name $name -Description $description -Condition ($cd1,$cd2) -AddRule ($rule1)
```

This command creates a task sequence "Set Dynamic Variable" step.

## PARAMETERS

### -AddRule

Specifies the rules and the order of the rules.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddRules

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Condition

Specifies the conditions.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Conditions

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

### -ContinueOnError

Indicates whether the operation continues when there is an error.

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

### -Description

Specifies a description.

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

### -Disable

Indicates whether the step shall be disabled.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableThisStep

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

### -Name

Specifies a name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StepName

Required: True
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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_SetDynamicVariablesAction

## NOTES

## RELATED LINKS

[Get-CMTSStepSetDynamicVariable](./Get-CMTSStepSetDynamicVariable.md)

[Set-CMTSStepSetDynamicVariable](./Set-CMTSStepSetDynamicVariable.md)

[Remove-CMTSStepSetDynamicVariable](./Remove-CMTSStepSetDynamicVariable.md)

[Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md)

[Set-CMTaskSequenceGroup](Set-CMTaskSequenceGroup.md)
