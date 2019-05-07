---
title: Set-CMGlobalConditionGeneral
titleSuffix: Configuration Manager
description: Modifies general settings for a Configuration Manager global condition.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Set-CMGlobalConditionGeneral

## SYNOPSIS

Modifies general settings for a Configuration Manager global condition.

## SYNTAX

```powershell
Set-CMGlobalConditionGeneral [-NewName <String>] [-Description <String>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

## DESCRIPTION

The **Set-CMGlobalConditionGeneral** cmdlet modifies general settings for a global condition.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1

```powershell
PS XYZ:\> Set-CMGlobalConditionGeneral -Name newscript -NewName newscript2 -Description Description2
```

This command modifies the name and the description.

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

### -NewName

Specifies a new name.

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

### -PassThru

Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## OUTPUTS

### System.Object

## RELATED LINKS

- [Set-CMGlobalCondition](./Set-CMGlobalCondition.md)
- [Set-CMGlobalConditionActiveDirectoryQuery](./Set-CMGlobalConditionActiveDirectoryQuery.md)
- [Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)
- [Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)
- [Set-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)
- [Set-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)
- [Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)
- [Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)
- [Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)
- [Set-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)
- [Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)
- [Set-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXPathQuery.md)
