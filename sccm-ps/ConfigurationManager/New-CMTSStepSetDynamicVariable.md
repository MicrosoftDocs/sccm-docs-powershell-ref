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

# New-CMTSStepSetDynamicVariable

## SYNOPSIS

{{Fill in the Synopsis}}

## SYNTAX

```powershell
New-CMTSStepSetDynamicVariable -AddRule <IResultObject[]> -Name <String> [-Description <String>]
 [-ContinueOnError] [-Disable] [-Condition <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm]
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

### -AddRule

{{Fill AddRule Description}}

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

{{Fill Condition Description}}

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

### -ContinueOnError

{{Fill ContinueOnError Description}}

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

{{Fill Description Description}}

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

{{Fill Disable Description}}

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

{{Fill DisableWildcardHandling Description}}

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

{{Fill ForceWildcardHandling Description}}

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

{{Fill Name Description}}

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

### None


## OUTPUTS

### IResultObject#SMS_TaskSequence_SetDynamicVariablesAction


## NOTES

## RELATED LINKS

* [Get-CMTSStepSetDynamicVariable](./Get-CMTSStepSetDynamicVariable.md)
* [Set-CMTSStepSetDynamicVariable](./Set-CMTSStepSetDynamicVariable.md)
* [Remove-CMTSStepSetDynamicVariable](./Remove-CMTSStepSetDynamicVariable.md)
