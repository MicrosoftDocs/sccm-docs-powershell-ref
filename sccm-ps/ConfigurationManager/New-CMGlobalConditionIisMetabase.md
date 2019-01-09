---
title: New-CMGlobalConditionIisMetabase
titleSuffix: Configuration Manager
description: Creates an IIS Metabase type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# New-CMGlobalConditionIisMetabase

## SYNOPSIS

Creates an IIS Metabase type global condition in Configuration Manager.

## SYNTAX

```powershell
New-CMGlobalConditionIisMetabase -DataType <GlobalConditionDataType> [-MetabasePath <String>]
 -PropertyId <Int32> -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

The **New-CMGlobalConditionIisMetabase** cmdlet creates an IIS Metabase type global condition in Microsoft System Center Configuration Manager.

A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

## EXAMPLES

### Example 1

```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -DataType

Specifies a data type.

```yaml
Type: GlobalConditionDataType
Parameter Sets: (All)
Aliases:
Accepted values: String, DateTime, Integer, FloatingPoint, Version, Boolean, StringArray

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

### -MetabasePath

Specifies a valid path to the IIS Metabase.

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

### -PropertyId

Specifies the numeric property of the IIS Metabase setting.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## OUTPUTS

### System.Object

## RELATED LINKS

- [Set-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)
- [New-CMGlobalCondition](./New-CMGlobalCondition.md)
- [New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)
- [New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)
- [New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)
- [New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)
- [New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)
- [New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)
- [New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)
- [New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)
- [New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)
- [New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)