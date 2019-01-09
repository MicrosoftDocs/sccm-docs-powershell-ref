---
title: New-CMGlobalConditionAssembly
titleSuffix: Configuration Manager
description: Creates an Assembly type global condition in Configuration Manager.

ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# New-CMGlobalConditionAssembly

## SYNOPSIS

Creates an Assembly type global condition in Configuration Manager.

## SYNTAX

```powershell
New-CMGlobalConditionAssembly -AssemblyName <String> -Name <String> [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

The **New-CMGlobalConditionAssembly** cmdlet creates an Assembly type global condition in Microsoft System Center Configuration Manager.

A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

## EXAMPLES

### Example 1

```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AssemblyName

Specifies the name of the assembly object to search for. The name cannot be the same as any other assembly object of the same type, and the name must be registered in the Global Assembly Cache. The assembly name can be a maximum of 256 characters.

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

## OUTPUTS

### System.Object

## RELATED LINKS

- [Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)
- [New-CMGlobalCondition](./New-CMGlobalCondition.md)
- [New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)
- [New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)
- [New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)
- [New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)
- [New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)
- [New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)
- [New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)
- [New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)
- [New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)
- [New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)

