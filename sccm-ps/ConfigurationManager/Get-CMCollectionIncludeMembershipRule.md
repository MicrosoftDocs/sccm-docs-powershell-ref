---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Get-CMCollectionIncludeMembershipRule
---

# Get-CMCollectionIncludeMembershipRule

## SYNOPSIS

Get an include membership rule for a device or user collection.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMCollectionIncludeMembershipRule -CollectionName <String> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String> [<CommonParameters>]
```

### ByIdAndName
```
Get-CMCollectionIncludeMembershipRule -CollectionId <String> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMCollectionIncludeMembershipRule -InputObject <IResultObject> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more include membership rules for a device or user collection.
An _include_ membership rule includes the members of another collection to the collections where the rule is applied.

Configuration Manager dynamically updates the membership of the collection on a schedule if the membership of the included collection changes.

For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all include membership rules

This command gets all include membership rules for the collection named **Device**.

```powershell
Get-CMCollectionIncludeMembershipRule -CollectionName "Device"
```

### Example 2: Get include membership rules by using the pipeline

This command first uses the **Get-CMCollection** to get the collection object named **Users**. It then uses the pipeline operator to pass the object to the **Get-CMCollectionIncludeMembershipRule** cmdlet, which gets all include membership rules for the collection object.

```powershell
Get-CMCollection -Name "Users" | Get-CMCollectionIncludeMembershipRule
```

## PARAMETERS

### -CollectionId

Specify the ID of the collection to get the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since default collections don't have include membership rules, this ID starts with the site code and not `SMS`.

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

### -IncludeCollection

Specify an object for the included collection to get the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

Specify the ID of the included collection to get the rule. This value is the **CollectionID** property, for example, `XYZ00012`. You can include default collections, so this value can start with either the site code or `SMS`.

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

Specify the name of the included collection to get the rule.

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

This cmdlet is similar to **Get-CMDeviceCollectionIncludeMembershipRule** and **Get-CMUserCollectionIncludeMembershipRule**, which are specific to the type of collection. This cmdlet works with either device or user collections.

## RELATED LINKS

[Remove-CMCollectionIncludeMembershipRule](Remove-CMCollectionIncludeMembershipRule.md)

[Get-CMCollectionDirectMembershipRule](Get-CMCollectionDirectMembershipRule.md)
[Get-CMCollectionExcludeMembershipRule](Get-CMCollectionExcludeMembershipRule.md)
[Get-CMCollectionQueryMembershipRule](Get-CMCollectionQueryMembershipRule.md)

[Add-CMDeviceCollectionIncludeMembershipRule](Add-CMDeviceCollectionIncludeMembershipRule.md)
[Add-CMUserCollectionIncludeMembershipRule](Add-CMUserCollectionIncludeMembershipRule.md)

[Get-CMDeviceCollectionIncludeMembershipRule](Get-CMDeviceCollectionIncludeMembershipRule.md)
[Get-CMUserCollectionIncludeMembershipRule](Get-CMUserCollectionIncludeMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
