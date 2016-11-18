---
external help file: AdminUI.PS.Collections-help.xml
online version: 
schema: 2.0.0
ms.assetid: A250BE6D-1C96-4337-88F5-454CB95B0AA1
---

# Get-CMDeviceCollectionQueryMembershipRule

## SYNOPSIS
Gets the query membership rules from one or more device collections in the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
Get-CMDeviceCollectionQueryMembershipRule -CollectionName <String> [-RuleName <String>] [<CommonParameters>]
```

### ById
```
Get-CMDeviceCollectionQueryMembershipRule -CollectionId <String> [-RuleName <String>] [<CommonParameters>]
```

### ByValue
```
Get-CMDeviceCollectionQueryMembershipRule -InputObject <IResultObject> [-RuleName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceCollectionQueryMembershipRule** cmdlet retrieves rules from the specified device collections.
You can specify the device collections where the rule is applied by names, IDs, or an input object that represents the device collections.
The query is specified by its ID or name.

A query rule lets you dynamically update the membership of a collection based on a query that is run on a schedule.
For more information about membership rules, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Get the query membership rules for a device collection
```
PS C:\>Get-CMUserCollectionQueryMembershipRule -CollectionName "Remote Users" -RuleName "Remote Users By Domain"
```

This command gets the query membership rule named Remote Users By Domain from device collection named Remote Users.

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
{{Fill InputObject Description}}

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

[Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433)

[Add-CMUserCollectionQueryMembershipRule](./Add-CMUserCollectionQueryMembershipRule.md)

[Remove-CMUserCollectionQueryMembershipRule](./Remove-CMUserCollectionQueryMembershipRule.md)

[Get-CMUserCollection](./Get-CMUserCollection.md)

[Get-CMDeviceCollection](./Get-CMDeviceCollection.md)


