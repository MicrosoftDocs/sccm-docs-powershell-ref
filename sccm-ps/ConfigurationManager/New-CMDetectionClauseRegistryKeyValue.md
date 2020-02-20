---
author: aczechowski
description: Creates a detection clause registry key value.
external help file: AdminUI.PS.Dcm.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMDetectionClauseRegistryKeyValue
titleSuffix: Configuration Manager
---

# New-CMDetectionClauseRegistryKeyValue

## SYNOPSIS
Creates a detection clause registry key value.

## SYNTAX

### Value
```
New-CMDetectionClauseRegistryKeyValue -ExpressionOperator <RuleExpressionOperator> -Hive <RegistryRootKey>
 [-Is64Bit] -KeyName <String> -PropertyType <SettingDataType> -ValueName <String> -ExpectedValue <String[]>
 [-Value] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseRegistryKeyValue -Hive <RegistryRootKey> [-Is64Bit] -KeyName <String>
 -PropertyType <SettingDataType> -ValueName <String> [-Existence] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

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

### -Existence
```yaml
Type: SwitchParameter
Parameter Sets: Existence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpectedValue
```yaml
Type: String[]
Parameter Sets: Value
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator
```yaml
Type: RuleExpressionOperator
Parameter Sets: Value
Aliases:
Accepted values: IsEquals, NotEquals, GreaterThan, GreaterEquals, LessThan, LessEquals, Between, OneOf, NoneOf, BeginsWith, EndsWith, NotEndsWith, Contains, NotContains

Required: True
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

### -Hive
```yaml
Type: RegistryRootKey
Parameter Sets: (All)
Aliases: RegistryHive
Accepted values: ClassesRoot, CurrentConfig, CurrentUser, LocalMachine, Users

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Is64Bit
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

### -KeyName
```yaml
Type: String
Parameter Sets: (All)
Aliases: RegistryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyType
```yaml
Type: SettingDataType
Parameter Sets: (All)
Aliases:
Accepted values: Version, Integer, String

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
```yaml
Type: SwitchParameter
Parameter Sets: Value
Aliases: ValueRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueName
```yaml
Type: String
Parameter Sets: (All)
Aliases: RegistryValueName

Required: True
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

### System.Object

## NOTES

## RELATED LINKS
