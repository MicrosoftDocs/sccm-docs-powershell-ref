---
description: Creates a detection clause windows installer.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/06/2019
schema: 2.0.0
title: New-CMDetectionClauseWindowsInstaller
---

# New-CMDetectionClauseWindowsInstaller

## SYNOPSIS
Creates a detection clause windows installer.

## SYNTAX

### Value
```
New-CMDetectionClauseWindowsInstaller -ExpectedValue <String> -ExpressionOperator <RuleExpressionOperator>
 -ProductCode <Guid> [-PropertyType <MSIProperty>] [-Value] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseWindowsInstaller -ProductCode <Guid> [-Existence] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

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
Type: String
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
Accepted values: IsEquals, NotEquals, GreaterEquals, GreaterThan, LessEquals, LessThan

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

### -ProductCode
```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyType
```yaml
Type: MSIProperty
Parameter Sets: Value
Aliases:
Accepted values: ProductVersion

Required: False
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
