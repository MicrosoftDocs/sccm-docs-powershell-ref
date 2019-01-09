---
title: New-CMGlobalConditionRegistryValue
titleSuffix: Configuration Manager
description: Creates a Registry Value type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# New-CMGlobalConditionRegistryValue

## SYNOPSIS

Creates a Registry Value type global condition in Configuration Manager.

## SYNTAX

```powershell
New-CMGlobalConditionRegistryValue -DataType <GlobalConditionDataType> [-Is64Bit <Boolean>]
 [-RegistryHive <RegistryRootKey>] -KeyName <String> [-ValueName <String>] -Name <String>
 [-Description <String>] -DeviceType <GlobalConditionDeviceType> [-DisableWildcardHandling]
 [-ForceWildcardHandling]
```

## DESCRIPTION

The **New-CMGlobalConditionRegistryValue** cmdlet creates a Registry Value type global condition in Microsoft System Center Configuration Manager.

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
Accepted values: String, DateTime, Integer, FloatingPoint, Version, StringArray

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

### -DeviceType

Specifies a device type.

```yaml
Type: GlobalConditionDeviceType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, WindowsMobile

Required: True
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

Specify the registry key name that you want to search for. The format used should be key\subkey.

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

### -ValueName

Specify the value that must be contained within the specified registry key.

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

- [Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)
- [New-CMGlobalCondition](./New-CMGlobalCondition.md)
- [New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)
- [New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)
- [New-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)
- [New-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)
- [New-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)
- [New-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)
- [New-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)
- [New-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)
- [New-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)
- [New-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXpathQuery.md)