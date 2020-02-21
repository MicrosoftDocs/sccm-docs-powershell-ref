---
author: aczechowski
description: Gets the maintenance windows for a collection.
external help file: AdminUI.PS.Collections.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMMaintenanceWindow
titleSuffix: Configuration Manager
---

# Get-CMMaintenanceWindow

## SYNOPSIS
Gets the maintenance windows for a collection.

## SYNTAX

### ByValue (Default)
```
Get-CMMaintenanceWindow [-InputObject] <IResultObject> [-MaintenanceWindowName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionId
```
Get-CMMaintenanceWindow [-CollectionId] <String> [-MaintenanceWindowName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionName
```
Get-CMMaintenanceWindow [-CollectionName] <String> [-MaintenanceWindowName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMaintenanceWindow** cmdlet gets the maintenance windows for specified collections.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get maintenance windows
```
PS XYZ:\> Get-CMMaintenanceWindow -CollectionID "AAA0004D"
```

This command gets the maintenance windows for the specified collection.

## PARAMETERS

### -CollectionId
Specifies an array of collection IDs.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
```yaml
Type: String
Parameter Sets: ByCollectionName
Aliases:

Required: True
Position: 0
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

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection, Site

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaintenanceWindowName
```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMMaintenanceWindow](New-CMMaintenanceWindow.md)

[Remove-CMMaintenanceWindow](Remove-CMMaintenanceWindow.md)

[Set-CMMaintenanceWindow](Set-CMMaintenanceWindow.md)


