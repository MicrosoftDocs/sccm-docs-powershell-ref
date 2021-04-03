---
description: Creates a WQL Query type global condition in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/08/2019
schema: 2.0.0
title: New-CMGlobalConditionWqlQuery
---

# New-CMGlobalConditionWqlQuery

## SYNOPSIS

Creates a WQL Query type global condition in Configuration Manager.

## SYNTAX

```
New-CMGlobalConditionWqlQuery -Class <String> -DataType <GlobalConditionDataType> [-Namespace <String>]
 -Property <String> [-WhereClause <String>] [-Description <String>] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMGlobalConditionWqlQuery** cmdlet creates a Wql Query type global condition in Configuration Manager.

A global condition is a setting or expression in Configuration Manager that you can use to specify how Configuration Manager provides and deploys an application to clients.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> $GlobalWql = New-CMGlobalConditionWqlQuery -DataType String -Class $aa -Property $aa -Namespace root\aaa -Name GC7
```

This command creates a WQL Query type global condition in Configuration Manager.

## PARAMETERS

### -Class

Specifies the WMI class that will be used to build a WQL query that will be assessed for compliance on client computers.

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

### -DataType

Specifies a data type.

```yaml
Type: GlobalConditionDataType
Parameter Sets: (All)
Aliases:
Accepted values: String, DateTime, Integer, FloatingPoint, Version, Boolean, StringArray, IntegerArray

Required: True
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
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace

Specifies the WMI namespace that will be used to build a WQL query that will be assessed for compliance on client computers. The default value is Root\cimv2.

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

### -Property

Specifies the WMI property that will be used to build a WQL query that will be assessed for compliance on client computers.

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

### -WhereClause

Specifies a WHERE clause to be applied to the specified namespace, class, and property on client computers.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)

[New-CMGlobalCondition](./New-CMGlobalCondition.md)

[New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)

[New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)

[New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)

[New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)

[New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)

[New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)

[New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)

[New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)

[New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)

[New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)
