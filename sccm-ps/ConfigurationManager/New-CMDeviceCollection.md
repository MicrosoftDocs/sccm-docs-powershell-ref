---
author: aczechowski
description: Creates a collection for devices and adds the collection to the Configuration Manager hierarchy.
external help file: AdminUI.PS.Collections-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMDeviceCollection
titleSuffix: Configuration Manager
---

# New-CMDeviceCollection

## SYNOPSIS
Creates a collection for devices and adds the collection to the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
New-CMDeviceCollection [-Comment <String>] -LimitingCollectionName <String> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
New-CMDeviceCollection [-Comment <String>] -InputObject <IResultObject> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
New-CMDeviceCollection [-Comment <String>] -LimitingCollectionId <String> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMDeviceCollection** cmdlet creates a collection based on a specific limiting collection.
The limiting collection determines which devices can be a member of the device collection that you create.
For instance, when you use the All Systems collection as the limiting collection, the new collection can include any device in the Configuration Manager hierarchy.
You specify the limiting collection by providing its name or ID.

Devices are added to the collection by membership rules.
To add members to the device collection use one of the following membership rule cmdlets:

- [Add-CMDeviceCollectionDirectMembershipRule](Add-CMDeviceCollectionDirectMembershipRule.md)
- [Add-CMDeviceCollectionExcludeMembershipRule](Add-CMDeviceCollectionExcludeMembershipRule.md)
- [Add-CMDeviceCollectionIncludeMembershipRule](Add-CMDeviceCollectionIncludeMembershipRule.md)
- [Add-CMDeviceCollectionQueryMembershipRule](Add-CMDeviceCollectionQueryMembershipRule.md)

Collections represent logical groupings of resources, such as users and devices.
For more information about Configuration Manager collections, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a device collection
```
PS XYZ:\> New-CMDeviceCollection -Name "Windows 7" -LimitingCollectionName "All Systems"
```

This command creates a collection for all computers that run Windows® 7.
The *LimitingCollectionName* parameter specifies that any device in the All Systems collection can be a member of the Windows® 7 collection.

## PARAMETERS

### -Comment
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

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: LimitingCollection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LimitingCollectionId
```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitingCollectionName
```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
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

### -RefreshSchedule
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshType
```yaml
Type: CollectionRefreshType
Parameter Sets: (All)
Aliases:
Accepted values: None, Manual, Periodic, Continuous, Both

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10))

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
