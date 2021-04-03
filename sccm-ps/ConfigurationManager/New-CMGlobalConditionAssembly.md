---
description: Creates an Assembly type global condition in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/08/2019
schema: 2.0.0
title: New-CMGlobalConditionAssembly
---

# New-CMGlobalConditionAssembly

## SYNOPSIS

Creates an Assembly type global condition in Configuration Manager.

## SYNTAX

```
New-CMGlobalConditionAssembly -AssemblyName <String> [-Description <String>] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMGlobalConditionAssembly** cmdlet creates an Assembly type global condition in Configuration Manager.

A global condition is a setting or expression in Configuration Manager that you can use to specify how Configuration Manager provides and deploys an application to clients.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> $GlobalAssembly =  New-CMGlobalConditionAssembly -AssemblyName $AssemblyName -Name GC2
```

This command creates an Assembly type global condition in Configuration Manager.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)

[New-CMGlobalCondition](./New-CMGlobalCondition.md)

[New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)

[New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)

[New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)

[New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)

[New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)

[New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)

[New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)

[New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)

[New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)

[New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)
