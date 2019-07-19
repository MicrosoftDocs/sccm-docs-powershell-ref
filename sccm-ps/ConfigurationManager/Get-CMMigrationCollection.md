<<<<<<< HEAD
---
title: Get-CMMigrationCollection
titleSuffix: Configuration Manager
description: Gets collections selected for migration.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Migration.dll-Help.xml
ms.assetid: ED0B8420-DCA5-43D7-A48B-45A539486580
online version: https://go.microsoft.com/fwlink/?linkid=833754
schema: 2.0.0
>>>>>>> master
---

# Get-CMMigrationCollection

## SYNOPSIS
Gets collections selected for migration.

## SYNTAX

### SearchById (Default)
```
Get-CMMigrationCollection [-Id <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMMigrationCollection [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMigrationCollection** cmdlet gets the collections selected from a source hierarchy for migration.
A collection is a set of resources in the Microsoft System Center Configuration Manager hierarchy.
A migration collection is the set of resources chosen from a hierarchy for migration, including related objects.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get a migration collection by name
```
PS XYZ:\> Get-CMMigrationCollection -Name "PhoneCollection5"
```

This command gets the migration collection.
The command specifies the value PhoneCollection5 for the *Name* parameter.

## PARAMETERS

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

### -Id
Specifies an identifier for a collection in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: CollectionEntityId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for a collection in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CollectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

