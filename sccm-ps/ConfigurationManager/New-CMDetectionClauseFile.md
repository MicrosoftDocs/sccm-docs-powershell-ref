---
description: Create a detection clause for a file in a configuration item.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/25/2020
schema: 2.0.0
title: New-CMDetectionClauseFile
---

# New-CMDetectionClauseFile

## SYNOPSIS

Create a detection clause for a file in a configuration item.

## SYNTAX

### Value
```
New-CMDetectionClauseFile -FileName <String> -PropertyType <FileFolderProperty> -ExpectedValue <String[]>
 -ExpressionOperator <RuleExpressionOperator> [-Is64Bit] -Path <String> [-Value] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseFile -FileName <String> [-Is64Bit] -Path <String> [-Existence] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a detection clause for a file in a configuration item.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Detect an application by version

This example detects the application **app.exe** in a specific folder where the version is greater than or equal to `1.0.0`.

```powershell
New-CMDetectionClauseFile -Path "C:\Program Files\Application" -FileName App.exe -Value -PropertyType Version -ExpressionOperator GreaterEquals -ExpectedValue "1.0.0"
```

## PARAMETERS

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

### -Existence

Add this parameter to create an existential rule type. For the setting to comply, the file exists on the client.

Alternatively, use the **-Value** parameter.

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

Specify an array of strings to compare the value. The value to compare depends upon the specified **PropertyType**.

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

For the **ExpectedValue**, specify the comparison operator.

```yaml
Type: RuleExpressionOperator
Parameter Sets: Value
Aliases:
Accepted values: IsEquals, NotEquals, GreaterThan, GreaterEquals, LessThan, LessEquals, Between, OneOf, NoneOf

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileName

Specify the file name to assess for compliance on clients. This string is just the file name. Use the **-Path** parameter to specify the folder path.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### -Is64Bit

Add this parameter to specify that this file is associated with a 64-bit application.

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

### -Path

Specify the folder path that contains the file to assess for compliance on clients. Use the **-FileName** parameter for the specific file.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyType

Specify the file property to compare and assess for compliance. Use the **-ExpectedValue** parameter to specify the value of this property, and the **-ExpressionOperator** parameter to specify the means of comparison.

For example, you set this parameter to `Version`, set **-ExpressionOperator** to `IsEquals`, and **-ExpectedValue** to `1.48.1.0`. The rule then checks the specified file to have that same file version.

```yaml
Type: FileFolderProperty
Parameter Sets: Value
Aliases:
Accepted values: DateCreated, DateModified, Version, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

Add this parameter to check compliance of a property value. Alternatively, use the **-Existence** parameter.

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
