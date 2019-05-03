---
title: Get-CMDeviceCollectionExcludeMembershipRule
titleSuffix: Configuration Manager
description: Gets the exclude membership rules from one or more device collections in the Configuration Manager hierarchy.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMDeviceCollectionExcludeMembershipRule

## SYNOPSIS
Gets the exclude membership rules from one or more device collections in the Configuration Manager hierarchy.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMDeviceCollectionExcludeMembershipRule -CollectionName <String> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMDeviceCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMDeviceCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMDeviceCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMDeviceCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndName
```
Get-CMDeviceCollectionExcludeMembershipRule -CollectionId <String> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMDeviceCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMDeviceCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMDeviceCollectionExcludeMembershipRule -InputObject <IResultObject> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceCollectionExcludeMembershipRule** cmdlet retrieves the rules that exclude the members of another collection from the device collections where the rule is applied.
You can specify the device collections where the rule is applied by name, ID, or an object that represents the collections.
You can specify the collection whose members are excluded by name, ID, or an object that represents the collection.

Microsoft System Center Configuration Manager dynamically updates the membership of the device collection on a schedule if the membership of the excluded collection changes.
For more information about membership rules, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Get the exclude membership rules from a device collection
```
PS C:\> Get-CMDeviceCollectionExcludeMembershipRule -CollectionId "9990000D" -ExcludeCollectionId "SMSDM001"
```

This command gets the rules that exclude the members of the collection that has the ID SMSDM001 from the device collection that has the ID 9990000D.

## PARAMETERS

### -CollectionId
```yaml
Type: String
Parameter Sets: ByIdAndValue, ByIdAndId, ByIdAndName
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
```yaml
Type: String
Parameter Sets: ByNameAndName, ByNameAndValue, ByNameAndId
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeCollection
```yaml
Type: IResultObject
Parameter Sets: ByNameAndValue, ByIdAndValue, ByValueAndValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeCollectionId
```yaml
Type: String
Parameter Sets: ByNameAndId, ByIdAndId, ByValueAndId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeCollectionName
```yaml
Type: String
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: ByValueAndValue, ByValueAndId, ByValueAndName
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433)

[Add-CMDeviceCollectionExcludeMembershipRule](Add-CMDeviceCollectionExcludeMembershipRule.md)

[Remove-CMDeviceCollectionExcludeMembershipRule](Remove-CMDeviceCollectionExcludeMembershipRule.md)


