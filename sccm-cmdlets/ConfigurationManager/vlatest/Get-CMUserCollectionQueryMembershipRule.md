---
external help file: AdminUI.PS.Collections-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833997
schema: 2.0.0
ms.assetid: FA669383-9E20-4F2B-B18E-1DB9BC3558C2
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
For more information about membership rules in Microsoft System Center Configuration Manager, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Get a rule by using a collection name
```
PS C:\> Get-CMUserCollectionQueryMembershipRule -CollectionName "Remote Users" -RuleName "Remote Users by Domain"
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMUserCollectionQueryMembershipRule](./Add-CMUserCollectionQueryMembershipRule.md)

[Get-CMUserCollection](./Get-CMUserCollection.md)

[Remove-CMUserCollectionQueryMembershipRule](./Remove-CMUserCollectionQueryMembershipRule.md)


