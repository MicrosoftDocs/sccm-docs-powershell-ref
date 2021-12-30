---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Get-CMUserCollectionDirectMembershipRule
---

# Get-CMUserCollectionDirectMembershipRule

## SYNOPSIS

Get a direct membership rule for a user collection.

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

Use this cmdlet to get one or more direct membership rules for a user collection.
A _direct_ membership rule lets you explicitly choose the members of the user collection.
Default collections don't have direct membership rules. Any collection that you target should have an ID that starts with the site code, not `SMS`.
For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all direct membership rules for a collection by name

This command gets the direct membership rules for the user collection named **Users**.

```powershell
Get-CMUserCollectionDirectMembershipRule -CollectionName "Users"
```

## PARAMETERS

### -CollectionId

Specify the ID of the user collection to get the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since default collections can't have direct membership rules, this ID starts with the site code and not `SMS`.

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

Specify the name of the user collection to get the rule.

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

Specify an object for the user collection to get the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

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

Specify a user object to get its direct membership rule from the user collection. To get this object, use the [Get-CMResource](Get-CMResource.md) or [Get-CMUser](Get-CMUser.md) cmdlets.

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

Specify the ID of the user to get its direct membership rule from the user collection. This value is the **ResourceID** property, for example `16777219`.

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

Specify the name of the user to get its direct membership rule from the user collection.

```yaml
Type: String
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)
[Remove-CMUserCollectionDirectMembershipRule](Remove-CMUserCollectionDirectMembershipRule.md)

[Get-CMCollectionDirectMembershipRule](Get-CMCollectionDirectMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)
[Get-CMResource](Get-CMResource.md)
[Get-CMUser](Get-CMUser.md)

[Get-CMDeviceCollectionDirectMembershipRule](Get-CMDeviceCollectionDirectMembershipRule.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
