---
title: New-CMTSRule
titleSuffix: Configuration Manager
description: Creates a new rule on a task sequence step in Configuration Manager.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---
# New-CMTSRule

## SYNOPSIS

Creates a new rule that can be added to task sequence steps.

## SYNTAX

### VariableOnly (Default)
```powershell
New-CMTSRule -Variable <hashtable> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ComputerCondition
```powershell
New-CMTSRule -Variable <hashtable> [-AssetTag <string>] [-MacAddress <string>] [-SerialNumber <string>]
 [-Uuid <string>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### LocationCondition
```powershell
New-CMTSRule -Variable <hashtable> [-DefaultGateway <string>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MakeModelCondition
```powershell
New-CMTSRule -Variable <hashtable> [-Make <string>] [-Model <string>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VariableCondition
```powershell
New-CMTSRule -Variable <hashtable> [-ReferencedVariableName <string>]
 [-ReferencedVariableOperator <VariableOperatorType>] [-ReferencedVariableValue <string>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Description

## EXAMPLES

### Example 1: Sets a task sequence variable to a value
```
PS XYZ:\> New-CMTSRule -Variable @{"MyTSVar" = 12345678}
```

## PARAMETERS

### -AssetTag


```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultGateway


```yaml
Type: String
Parameter Sets: LocationCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MacAddress


```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Make


```yaml
Type: String
Parameter Sets: MakeModelCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Model


```yaml
Type: String
Parameter Sets: MakeModelCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableName


```yaml
Type: String
Parameter Sets: VariableCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableOperator


```yaml
Type: String
Parameter Sets: VariableCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableValue


```yaml
Type: String
Parameter Sets: VariableCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SerialNumber


```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uuid


```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable


```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Variables

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).
