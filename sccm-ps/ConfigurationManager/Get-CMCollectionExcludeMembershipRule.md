---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Get-CMCollectionExcludeMembershipRule
---

# Get-CMCollectionExcludeMembershipRule

## SYNOPSIS

Get an exclude membership rule for a device or user collection.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMCollectionExcludeMembershipRule -CollectionName <String> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollectionId <String> [<CommonParameters>]
```

### ByIdAndName
```
Get-CMCollectionExcludeMembershipRule -CollectionId <String> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMCollectionExcludeMembershipRule -InputObject <IResultObject> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more exclude membership rules for a device or user collection.
An _exclude_ membership rule excludes the members of another collection from the collections where the rule is applied.

Configuration Manager dynamically updates the membership of the collection on a schedule if the membership of the excluded collection changes.

For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the exclude membership rules for a collection

This command gets the rules that exclude the members of the collection with ID **SMSDM001** from the collection with ID **XYZ00012**.

```powershell
Get-CMCollectionExcludeMembershipRule -CollectionId "XYZ00012" -ExcludeCollectionId "SMSDM001"
```

## PARAMETERS

### -CollectionId

Specify the ID of the collection to get the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since default collections don't have exclude membership rules, this ID starts with the site code and not `SMS`.

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

Specify the name of the collection to get the rule.

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

Specify an object for the excluded collection to get the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

Specify the ID of the excluded collection to get the rule. This value is the **CollectionID** property, for example, `XYZ00012`. You can exclude default collections, so this value can start with either the site code or `SMS`.

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

Specify the name of the excluded collection to get the rule.

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

Specify an object for the collection to get the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

This cmdlet is similar to **Get-CMDeviceCollectionExcludeMembershipRule** and **Get-CMUserCollectionExcludeMembershipRule**, which are specific to the type of collection. This cmdlet works with either device or user collections.

## RELATED LINKS

[Remove-CMCollectionExcludeMembershipRule](Remove-CMCollectionExcludeMembershipRule.md)

[Get-CMCollectionDirectMembershipRule](Get-CMCollectionDirectMembershipRule.md)
[Get-CMCollectionIncludeMembershipRule](Get-CMCollectionIncludeMembershipRule.md)
[Get-CMCollectionQueryMembershipRule](Get-CMCollectionQueryMembershipRule.md)

[Add-CMDeviceCollectionExcludeMembershipRule](Add-CMDeviceCollectionExcludeMembershipRule.md)
[Add-CMUserCollectionExcludeMembershipRule](Add-CMUserCollectionExcludeMembershipRule.md)

[Get-CMDeviceCollectionExcludeMembershipRule](Get-CMDeviceCollectionExcludeMembershipRule.md)
[Get-CMUserCollectionExcludeMembershipRule](Get-CMUserCollectionExcludeMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
