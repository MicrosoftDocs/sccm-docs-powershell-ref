---
title: New-CMTSStepConditionVariable
titleSuffix: Configuration Manager
description: Creates a t s step condition variable.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# New-CMTSStepConditionVariable

## SYNOPSIS
Creates a t s step condition variable.

## SYNTAX

```
New-CMTSStepConditionVariable -OperatorType <VariableOperatorType> -ConditionVariableName <String>
 [-ConditionVariableValue <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
```

 

## PARAMETERS

### -ConditionVariableName
 

```yaml
Type: String
Parameter Sets: (All)
Aliases: Variable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConditionVariableValue
 

```yaml
Type: String
Parameter Sets: (All)
Aliases: Value

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

### -OperatorType
 

```yaml
Type: VariableOperatorType
Parameter Sets: (All)
Aliases: Condition
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual, Like

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_VariableConditionExpression

## NOTES

## RELATED LINKS

