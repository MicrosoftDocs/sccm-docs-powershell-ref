---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Get-CMCollectionDirectMembershipRule
---

# Get-CMCollectionDirectMembershipRule

## SYNOPSIS

Get a direct membership rule for a device or user collection.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMCollectionDirectMembershipRule -CollectionName <String> [-ResourceName <String>] [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject> [<CommonParameters>]
```

### ByNameAndId
```
Get-CMCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String> [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject> [<CommonParameters>]
```

### ByIdAndId
```
Get-CMCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String> [<CommonParameters>]
```

### ByIdAndName
```
Get-CMCollectionDirectMembershipRule -CollectionId <String> [-ResourceName <String>] [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String> [<CommonParameters>]
```

### ByValueAndName
```
Get-CMCollectionDirectMembershipRule -InputObject <IResultObject> [-ResourceName <String>] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more direct membership rules for a device or user collection.
A _direct_ membership rule lets you explicitly choose the members of the device collection.
Default collections don't have direct membership rules. Any collection that you target should have an ID that starts with the site code, not `SMS`.
For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all direct membership rules for a collection by name

This command gets the direct membership rules for the collection named **Device01**.

```powershell
Get-CMCollectionDirectMembershipRule -CollectionName "Device01"
```

### Example 2: Get all direct membership rules by using the pipeline

This command uses the **Get-CMCollection** cmdlet to get the collection object named **User02**. It then uses the pipeline operator to pass the object to the **Get-CMCollectionDirectMembershipRule** cmdlet.

```powershell
Get-CMCollection -Name "User02" | Get-CMCollectionDirectMembershipRule
```

## PARAMETERS

### -CollectionId

Specify the ID of the collection to get the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since default collections can't have direct membership rules, this ID starts with the site code and not `SMS`.

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

### -Resource

Specify a resource, device, or user object to get its direct membership rule from the collection. To get this object, use the [Get-CMResource](Get-CMResource.md), [Get-CMDevice](Get-CMDevice.md), or [Get-CMUser](Get-CMUser.md) cmdlets.

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

Specify the ID of the resource to get its direct membership rule from the collection. This value is the **ResourceID** property, for example `16777219`.

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

Specify the name of the device or user to get its direct membership rule from the collection.

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

This cmdlet is similar to **Get-CMDeviceCollectionDirectMembershipRule** and **Get-CMUserCollectionDirectMembershipRule**, which are specific to the type of collection. This cmdlet works with either device or user collections.

## RELATED LINKS

[Remove-CMCollectionDirectMembershipRule](Remove-CMCollectionDirectMembershipRule.md)

[Get-CMCollectionExcludeMembershipRule](Get-CMCollectionExcludeMembershipRule.md)
[Get-CMCollectionIncludeMembershipRule](Get-CMCollectionIncludeMembershipRule.md)
[Get-CMCollectionQueryMembershipRule](Get-CMCollectionQueryMembershipRule.md)

[Add-CMDeviceCollectionDirectMembershipRule](Add-CMDeviceCollectionDirectMembershipRule.md)
[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)

[Get-CMDeviceCollectionDirectMembershipRule](Get-CMDeviceCollectionDirectMembershipRule.md)
[Get-CMUserCollectionDirectMembershipRule](Get-CMUserCollectionDirectMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)

[Get-CMResource](Get-CMResource.md)
[Get-CMDevice](Get-CMDevice.md)
[Get-CMUser](Get-CMUser.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
