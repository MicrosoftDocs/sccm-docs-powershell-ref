---
author: aczechowski
description: Imports a Configuration Manager collection.
external help file: AdminUI.PS.Collections.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Import-CMCollection
titleSuffix: Configuration Manager
---

# Import-CMCollection

## SYNOPSIS
Imports a Configuration Manager collection.

## SYNTAX

```
Import-CMCollection [-ImportFilePath] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMCollection** cmdlet imports a previously exported collection into Microsoft System Center Configuration Manager.

Configuration Manager collections provide a way to manage users, computers, and other resources in your organization. They not only give you a means to organize your resources, but they also give you a means to distribute Configuration Manager packages to clients and users.

## EXAMPLES

### Example 1: Import a collection
```
PS XYZ:\> Import-CMCollection -ImportFilePath "c:\path\collection.mof"
```

This command imports the collection defined in the collection.mof file.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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

### -ImportFilePath
Specifies the full path of the import (MOF) file for the collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 0
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCollection](Get-CMCollection.md)

[Export-CMCollection](Export-CMCollection.md)

[New-CMCollection](New-CMCollection.md)

[Remove-CMCollection](Remove-CMCollection.md)

[Set-CMCollection](Set-CMCollection.md)


