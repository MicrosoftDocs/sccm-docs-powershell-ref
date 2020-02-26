---
description: Creates a Registry Value type global condition in Configuration Manager.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/08/2019
schema: 2.0.0
title: New-CMGlobalConditionRegistryValue
---

# New-CMGlobalConditionRegistryValue

## SYNOPSIS

Creates a Registry Value type global condition in Configuration Manager.

## SYNTAX

```
New-CMGlobalConditionRegistryValue -DataType <GlobalConditionDataType> [-Is64Bit <Boolean>]
 [-RegistryHive <RegistryRootKey>] -KeyName <String> [-ValueName <String>] -Name <String>
 [-Description <String>] -DeviceType <GlobalConditionDeviceType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMGlobalConditionRegistryValue** cmdlet creates a Registry Value type global condition in Microsoft System Center Configuration Manager.

A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
$GlobalRegValue = New-CMGlobalConditionRegistryValue -DataType String -KeyName key -Name GC4 -DeviceType WindowsMobile -RegistryHive LocalMachine -ValueName VName
```

This command creates a Registry Value type global condition in Configuration Manager.

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

Specifies the value that must be contained within the specified registry key.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)

[New-CMGlobalCondition](./New-CMGlobalCondition.md)

[New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)

[New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)

[New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)

[New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)

[New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)

[New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)

[New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)

[New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)

[New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)

[New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)
