<<<<<<< HEAD
---
title: Get-CMComputerAssociation
titleSuffix: Configuration Manager
description: Gets Configuration Manager computer associations.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: 621E70A5-817B-46A2-ADEA-3D5F5012788F
online version: https://go.microsoft.com/fwlink/?linkid=834259
schema: 2.0.0
>>>>>>> master
---

# Get-CMComputerAssociation

## SYNOPSIS
Gets Configuration Manager computer associations.

## SYNTAX

### SearchByName (Default)
```
Get-CMComputerAssociation [-DestinationComputer <String>] [-SourceComputer <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMComputerAssociation -MigrationId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMComputerAssociation** cmdlet gets computer associations.
Microsoft System Center Configuration Manager uses a computer association to migrate user state and settings as part of operating system deployment.
You can specify a source computer, a destination computer, or both.
You can also use an ID to specify a computer association.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get all computer associations
```
PS XYZ:\> Get-CMComputerAssociation
```

This command gets all the computer associations for System Center Configuration Manager.

### Example 2: Get computer associations for a destination comptuter
```
PS XYZ:\> Get-CMComputerAssociation -DestinationComputer "West155"
```

This command gets all the computer associations for the destination computer named West155.

### Example 3: Get a computer association by using an ID
```
PS XYZ:\> Get-CMComputerAssociation -MigrationId "MID1207"
```

This command gets the computer association that has the ID MID1207.

## PARAMETERS

### -DestinationComputer
Specifies the name of a destination computer.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: RestoreName

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

### -MigrationId
Specifies the ID of a computer association.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceComputer
Specifies the name of a source computer.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: SourceName

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

[New-CMComputerAssociation](New-CMComputerAssociation.md)

[Remove-CMComputerAssociation](Remove-CMComputerAssociation.md)

[Set-CMComputerAssociation](Set-CMComputerAssociation.md)


