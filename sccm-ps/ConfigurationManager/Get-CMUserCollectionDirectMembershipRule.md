---
description: Gets the direct membership rules of one or more user collections in the Configuration Manager hierarchy.
external help file: AdminUI.PS.Collections-help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMUserCollectionDirectMembershipRule
---

# Get-CMUserCollectionDirectMembershipRule

## SYNOPSIS
Gets the direct membership rules of one or more user collections in the Configuration Manager hierarchy.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMUserCollectionDirectMembershipRule -CollectionName <String> [-ResourceName <String>] [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMUserCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMUserCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String> [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMUserCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject> [<CommonParameters>]
```

### ByIdAndId
```
Get-CMUserCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String> [<CommonParameters>]
```

### ByIdAndName
```
Get-CMUserCollectionDirectMembershipRule -CollectionId <String> [-ResourceName <String>] [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String> [<CommonParameters>]
```

### ByValueAndName
```
Get-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> [-ResourceName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserCollectionDirectMembershipRule** cmdlet retrieves the direct rules of the specified collections.
You can specify the user collections by using their names, IDs, or by specifying an object that represents the collections.

A direct rule lets you explicitly choose the members of the user collection.
For more information about collection rules, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a direct membership rule
```
PS XYZ:\> Get-CMUserCollectionDirectMembershipRule -CollectionName "All Mobile Devices" -ResourceId "Res_94412512"
```

This command gets the direct membership rule that has the Id Res_94412512 for the collection named All Mobile Devices.

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

### -Resource
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

### -ResourceId
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

### -ResourceName
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Remove-CMUserCollectionDirectMembershipRule](Remove-CMUserCollectionDirectMembershipRule.md)


