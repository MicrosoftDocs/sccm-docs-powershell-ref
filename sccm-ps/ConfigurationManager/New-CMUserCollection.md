---
title: New-CMUserCollection
titleSuffix: Configuration Manager
description: Creates a collection for users and adds the collection to the Configuration Manager hierarchy.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# New-CMUserCollection

## SYNOPSIS
Creates a collection for users and adds the collection to the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
New-CMUserCollection [-Comment <String>] -LimitingCollectionName <String> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
New-CMUserCollection [-Comment <String>] -InputObject <IResultObject> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
New-CMUserCollection [-Comment <String>] -LimitingCollectionId <String> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMUserCollection** cmdlet creates a collection based on a specific limiting collection.
The limiting collection determines which users can be a member of the user collection that you create.
For example, when you use the All Users collection as the limiting collection, the new collection can include any user in the Microsoft System Center Configuration Manager hierarchy.
You specify the limiting collection by providing its name or ID.

Users are added to the collection by membership rules.
To add members to the user collection use one of the following membership rule cmdlets: 

- Add-CMDeviceCollectionQueryMembershipRule
- Add-CMUserCollectionDirectMembershipRule
- Add-CMUserCollectionExcludeMembershipRule
- Add-CMUserCollectionIncludeMembershipRule

Collections represent logical groupings of resources, such as users and devices.
For more information about Configuration Manager collections, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Create a user collection
```
PS C:\> New-CMUserCollection -Name "Sales" -LimitingCollectionName "All Users"
```

This command creates a collection for all users in the Sales department.
Specifying All Users for the *LimitingCollectionName* parameter indicates that the new collection can include any user in the Configuration Manager hierarchy.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMDeviceCollectionQueryMembershipRule](Add-CMDeviceCollectionQueryMembershipRule.md)

[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)

[Add-CMUserCollectionExcludeMembershipRule](Add-CMUserCollectionExcludeMembershipRule.md)

[Add-CMUserCollectionIncludeMembershipRule](Add-CMUserCollectionIncludeMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)


