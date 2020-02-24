---
author: aczechowski
description: Gets one or more user collections in the Configuration Manager hierarchy.
external help file: AdminUI.PS.Collections-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMUserCollection
titleSuffix: Configuration Manager
---

# Get-CMUserCollection

## SYNOPSIS
Gets one or more user collections in the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
Get-CMUserCollection [-Name <String>] [<CommonParameters>]
```

### ById
```
Get-CMUserCollection -Id <String> [<CommonParameters>]
```

### ByDPGroupName
```
Get-CMUserCollection -DistributionPointGroupName <String> [<CommonParameters>]
```

### ByDPGroupId
```
Get-CMUserCollection -DistributionPointGroupId <String> [<CommonParameters>]
```

### ByDPGroup
```
Get-CMUserCollection -DistributionPointGroup <IResultObject> [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserCollection** cmdlet retrieves collections that contain users in Microsoft System Center Configuration Manager.
For more information about collections, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a user collection
```
PS XYZ:\> Get-CMUserCollection -CollectionId "9990000D"
```

This command gets the user collection that has the ID 9990000D.

## PARAMETERS

### -DistributionPointGroup
```yaml
Type: IResultObject
Parameter Sets: ByDPGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupId
```yaml
Type: String
Parameter Sets: ByDPGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
```yaml
Type: String
Parameter Sets: ByDPGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
```yaml
Type: String
Parameter Sets: ById
Aliases: CollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: ByName
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

## NOTES

## RELATED LINKS

[New-CMUserCollection](New-CMUserCollection.md)


