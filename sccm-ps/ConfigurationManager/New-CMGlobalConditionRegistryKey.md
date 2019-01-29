---
title: New-CMGlobalConditionRegistryKey
titleSuffix: Configuration Manager
description: Creates a Registry Key type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# New-CMGlobalConditionRegistryKey

## SYNOPSIS

Creates a Registry Key type global condition in Configuration Manager.

## SYNTAX

```powershell
New-CMGlobalConditionRegistryKey [-Is64Bit <Boolean>] [-RegistryHive <RegistryRootKey>] -KeyName <String>
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

The **New-CMGlobalConditionRegistryKey** cmdlet creates a Registry Key type global condition in Microsoft System Center Configuration Manager.

A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

## EXAMPLES

### Example 1

```powershell
PS C:\> $GlobalRegKey = New-CMGlobalConditionRegistryKey -KeyName key -Name GC3 -RegistryHive LocalMachine -Description $String
```

This command creates a Registry Key type global condition in Configuration Manager.

## PARAMETERS

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

### -Is64Bit

Specifies whether the 64-bit registry keys should be searched in addition to the 32-bit registry keys on clients that run a 64-bit version of Windows.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyName

Specifies the registry key name that you want to search for. The format used should be key\subkey.

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

### -Name

Specifies a nem.

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

### -RegistryHive

Specifies the registry hive that you want to search in.

```yaml
Type: RegistryRootKey
Parameter Sets: (All)
Aliases:
Accepted values: ClassesRoot, CurrentConfig, CurrentUser, LocalMachine, Users

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## OUTPUTS

### System.Object

## RELATED LINKS

- [Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)
- [New-CMGlobalCondition](./New-CMGlobalCondition.md)
- [New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)
- [New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)
- [New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)
- [New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)
- [New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)
- [New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)
- [New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)
- [New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)
- [New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)
- [New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)