---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Get-CMCollection
---

# Get-CMCollection

## SYNOPSIS

Get a device or user collection object.

## SYNTAX

### ByName (Default)
```
Get-CMCollection [-CollectionType <CollectionType>] [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByDPGroup
```
Get-CMCollection [-CollectionType <CollectionType>] -DistributionPointGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByDPGroupId
```
Get-CMCollection [-CollectionType <CollectionType>] -DistributionPointGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByDPGroupName
```
Get-CMCollection [-CollectionType <CollectionType>] -DistributionPointGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollection [-CollectionType <CollectionType>] -Id <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a device or user collection object.

Collections help you organize resources into manageable units. You can create collections to match your client management needs, and to perform operations on multiple resources at one time. Most management tasks rely on or require using one or more collections.

To scope the type of collection that you get, use the [Get-CMDeviceCollection](Get-CMDeviceCollection.md) or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

If you don't specify a collection by name, ID or object, this cmdlet returns all collections.

For more information, see [Introduction to collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a collection by name

This command gets the collection named **testUser**.

```powershell
Get-CMCollection -Name "testUser"
```

### Example 2: Get a collection for a distribution point group

This command gets the distribution point group object named **dpg1** and uses the pipeline operator to pass the object to **Get-CMCollection**, which gets the collections associated with the distribution point group.

```powershell
Get-CMDistributionPointGroup -Name "dpg1" | Get-CMCollection
```

When you distribute content to these collections, the site automatically distributes to all current members of this distribution point group. For more information, see [Manage distribution point groups](/mem/configmgr/core/servers/deploy/configure/install-and-configure-distribution-points#bkmk_manage).

## PARAMETERS

### -CollectionType

Filter the type of collection to get. This parameter is functionally the same as using the [Get-CMDeviceCollection](Get-CMDeviceCollection.md) or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

```yaml
Type: CollectionType
Parameter Sets: (All)
Aliases:
Accepted values: User, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroup

Specify a distribution point group object that's associated with this collection. To get this object, use the [Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByDPGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroupId

Specify the GUID for a distribution point group that's associated with this collection. This value is the **GroupID** property, which is a standard GUID surrounded by curly brackets, for example, `{537e6303-69eb-4104-bf7b-7baf43ce2352}`.

```yaml
Type: String
Parameter Sets: ByDPGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName

Specify the name of a distribution point group that's associated with this collection.

```yaml
Type: String
Parameter Sets: ByDPGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

Specify the ID of the collection to get. This value is the **CollectionID** property, for example, `XYZ00012` or `SMS00001`.

```yaml
Type: String
Parameter Sets: ById
Aliases: CollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the collection to get.

```yaml
Type: String
Parameter Sets: ByName
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

### IResultObject[]#SMS_Collection
### IResultObject#SMS_Collection

## NOTES

For more information on this return object and its properties, see [SMS_Collection server WMI class](/mem/configmgr/develop/reference/core/clients/collections/sms_collection-server-wmi-class).

## RELATED LINKS

[Copy-CMCollection](Copy-CMCollection.md)
[Export-CMCollection](Export-CMCollection.md)
[Get-CMCollectionMember](Get-CMCollectionMember.md)
[Get-CMCollectionSetting](Get-CMCollectionSetting.md)
[Import-CMCollection](Import-CMCollection.md)
[Invoke-CMCollectionUpdate](Invoke-CMCollectionUpdate.md)
[New-CMCollection](New-CMCollection.md)
[Remove-CMCollection](Remove-CMCollection.md)
[Set-CMCollection](Set-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)

[Introduction to collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections)
