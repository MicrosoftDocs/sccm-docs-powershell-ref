---
description: Gets the query membership rules from one or more user collections in the Configuration Manager hierarchy.
external help file: AdminUI.PS.Collections-help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMUserCollectionQueryMembershipRule
---

# Get-CMUserCollectionQueryMembershipRule

## SYNOPSIS
Gets the query membership rules from one or more user collections in the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
Get-CMUserCollectionQueryMembershipRule -CollectionName <String> [-RuleName <String>] [<CommonParameters>]
```

### ById
```
Get-CMUserCollectionQueryMembershipRule -CollectionId <String> [-RuleName <String>] [<CommonParameters>]
```

### ByValue
```
Get-CMUserCollectionQueryMembershipRule -InputObject <IResultObject> [-RuleName <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserCollectionQueryMembershipRule** cmdlet retrieves rules from the specified user collections.
You can specify the user collections where the rule is applied by using their names, IDs, or by specifying an input object that represents the user collections.
The query is specified by its ID or name.

A query rule lets you dynamically update the membership of a collection based on a query that is run on a schedule.
For more information about membership rules in Microsoft System Center Configuration Manager, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a rule by using a collection name
```
PS XYZ:\> Get-CMUserCollectionQueryMembershipRule -CollectionName "Remote Users" -RuleName "Remote Users by Domain"
```

This command gets the rule named Remote Users by Domain that belongs to the collection named Remote Users.

## PARAMETERS

### -CollectionId
```yaml
Type: String
Parameter Sets: ById
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
Parameter Sets: ByName
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
Parameter Sets: ByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RuleName
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMUserCollectionQueryMembershipRule](Add-CMUserCollectionQueryMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Remove-CMUserCollectionQueryMembershipRule](Remove-CMUserCollectionQueryMembershipRule.md)


