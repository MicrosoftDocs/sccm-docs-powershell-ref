---
author: mumian
description: Sets a IIS Metabase type global condition in Configuration Manager.
external help file: AdminUI.PS.Dcm.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: jgao
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
schema: 2.0.0
title: Set-CMGlobalConditionIisMetabase
titleSuffix: Configuration Manager
---

# Set-CMGlobalConditionIisMetabase

## SYNOPSIS

Sets a IIS Metabase type global condition in Configuration Manager.

## SYNTAX

```
Set-CMGlobalConditionIisMetabase [-MetabasePath <String>] [-PropertyId <Int32>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMGlobalConditionIisMetabase** cmdlet modifies settings for an IIS Metabase type global condition in Microsoft System Center Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> $GlobalIIS = Set-CMGlobalConditionIisMetabase -DataType String -PropertyId $int -Name GC3
```

This command sets a IIS Metabase type global condition in Configuration Manager.

## PARAMETERS

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

### -PropertyId

Specifies the numeric property of the IIS Metabase setting.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)

[Set-CMGlobalCondition](./Set-CMGlobalCondition.md)

[Set-CMGlobalConditionActiveDirectoryQuery](./Set-CMGlobalConditionActiveDirectoryQuery.md)

[Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)

[Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)

[Set-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)

[Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)

[Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)

[Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)

[Set-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)

[Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)

[Set-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXPathQuery.md)
