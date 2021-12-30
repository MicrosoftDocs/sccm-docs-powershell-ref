---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Get-CMDeviceCollectionIncludeMembershipRule
---

# Get-CMDeviceCollectionIncludeMembershipRule

## SYNOPSIS

Get an include membership rule for a device collection.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndName
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more include membership rules for a device collection.
An _include_ membership rule includes the members of another collection to the device collections where the rule is applied.

Configuration Manager dynamically updates the membership of the device collection on a schedule if the membership of the included collection changes.

For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all include membership rules

This command gets all include membership rules for the collection named **Device**.

```powershell
Get-CMDeviceCollectionIncludeMembershipRule -CollectionName "Device"
```

### Example 2: Get include membership rules by using the pipeline

This command first uses the **Get-CMCollection** to get the device collection object named **Device**. It then uses the pipeline operator to pass the object to the **Get-CMDeviceCollectionIncludeMembershipRule** cmdlet, which gets all include membership rules for the device collection object.

```powershell
Get-CMCollection -Name "Device" | Get-CMDeviceCollectionIncludeMembershipRule
```

## PARAMETERS

### -CollectionId

Specify the ID of the device collection to get the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since default collections don't have include membership rules, this ID starts with the site code and not `SMS`.

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

Specify the name of the device collection to get the rule.

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

Specify an object for the included collection to get the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

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

Specify an object for the device collection to get the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

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

## RELATED LINKS

[Add-CMDeviceCollectionIncludeMembershipRule](Add-CMDeviceCollectionIncludeMembershipRule.md)
[Remove-CMDeviceCollectionIncludeMembershipRule](Remove-CMDeviceCollectionIncludeMembershipRule.md)

[Get-CMCollectionIncludeMembershipRule](Get-CMCollectionIncludeMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Get-CMUserCollectionIncludeMembershipRule](Get-CMUserCollectionIncludeMembershipRule.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
