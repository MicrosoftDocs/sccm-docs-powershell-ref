---
description: Gets the exclude membership rules from one or more user collections in the Configuration Manager hierarchy.
external help file: AdminUI.PS.Collections-help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMUserCollectionExcludeMembershipRule
---

# Get-CMUserCollectionExcludeMembershipRule

## SYNOPSIS
Gets the exclude membership rules from one or more user collections in the Configuration Manager hierarchy.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMUserCollectionExcludeMembershipRule -CollectionName <String> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMUserCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMUserCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMUserCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMUserCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndName
```
Get-CMUserCollectionExcludeMembershipRule -CollectionId <String> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMUserCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMUserCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMUserCollectionExcludeMembershipRule -InputObject <IResultObject> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserCollectionExcludeMembershipRule** cmdlet retrieves the rules that exclude the members of another collection from the user collections where the rule is applied.
You can specify the user collections where the rule is applied by using their names, IDs, or by specifying an object that represents the collections.
You can specify the collection whose members are excluded by using its name, ID, or an object that represents the collection.

Microsoft System Center Configuration Manager dynamically updates the membership of the user collection on a schedule if the membership of the excluded collection changes.
For more information about membership rules, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get the exclude membership rule from a user collection
```
PS XYZ:\> Get-CMUserCollectionExcludeMembershipRule -CollectionId "9990000D" -ExcludeCollectionId "SMSDM001"
```

This command gets the rule that excludes the members of the collection that has the ID SMSDM001 from the user collection that has the ID 9990000D.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMUserCollectionExcludeMembershipRule](Add-CMUserCollectionExcludeMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Remove-CMUserCollectionExcludeMembershipRule](Remove-CMUserCollectionExcludeMembershipRule.md)


