---
author: aczechowski
description: Gets the include membership rules from one or more user collections in the Configuration Manager hierarchy.
external help file: AdminUI.PS.Collections-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMUserCollectionIncludeMembershipRule
titleSuffix: Configuration Manager
---

# Get-CMUserCollectionIncludeMembershipRule

## SYNOPSIS
Gets the include membership rules from one or more user collections in the Configuration Manager hierarchy.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMUserCollectionIncludeMembershipRule -CollectionName <String> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMUserCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMUserCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMUserCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMUserCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndName
```
Get-CMUserCollectionIncludeMembershipRule -CollectionId <String> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMUserCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMUserCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMUserCollectionIncludeMembershipRule -InputObject <IResultObject> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserCollectionIncludeMembershipRule** cmdlet retrieves rules that include the members of another collection in the user collections where the rule is applied.
You can specify the user collections where the rule is applied by using their names, IDs, or by specifying an object that represents the collections.

Microsoft System Center Configuration Manager dynamically updates the membership of the user collection if the membership of the included collection changes.
For more information about membership rules, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get the include membership rules from a user collection
```
PS XYZ:\> Get-CMUserCollectionIncludeMembershipRule -CollectionId "9990000D" -IncludeCollectionId "SMSDM001"
```

This command gets the include membership rules for the collection that has the ID SMSDM001 from the user collection that has the ID 9990000D.

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

### -IncludeCollection
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

### -IncludeCollectionId
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

### -IncludeCollectionName
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMUserCollectionIncludeMembershipRule](Add-CMUserCollectionIncludeMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Remove-CMUserCollectionIncludeMembershipRule](Remove-CMUserCollectionIncludeMembershipRule.md)


