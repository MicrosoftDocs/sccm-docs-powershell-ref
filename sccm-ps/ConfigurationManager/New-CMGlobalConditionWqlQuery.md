---
title: New-CMGlobalConditionWqlQuery
titleSuffix: Configuration Manager
description: Creates a WQL Query type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# New-CMGlobalConditionWqlQuery

## SYNOPSIS

Creates a WQL Query type global condition in Configuration Manager.

## SYNTAX

```powershell
New-CMGlobalConditionWqlQuery -DataType <GlobalConditionDataType> [-Namespace <String>] -Class <String>
 -Property <String> [-WhereClause <String>] -Name <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling]
```

## DESCRIPTION

The **New-CMGlobalConditionWqlQuery** cmdlet creates a Wql Query type global condition in Microsoft System Center Configuration Manager.

A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

## EXAMPLES

### Example 1

```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

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

Specify the WMI namespace that will be used to build a WQL query that will be assessed for compliance on client computers. The default value is Root\cimv2.

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

## OUTPUTS

### System.Object

## RELATED LINKS

- [Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)
- [New-CMGlobalCondition](./New-CMGlobalCondition.md)
- [New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)
- [New-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)
- [New-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)
- [New-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)
- [New-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)
- [New-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)
- [New-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)
- [New-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)
- [New-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXpathQuery.md)