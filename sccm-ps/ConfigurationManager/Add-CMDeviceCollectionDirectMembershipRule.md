---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Add-CMDeviceCollectionDirectMembershipRule
---

# Add-CMDeviceCollectionDirectMembershipRule

## SYNOPSIS

Add a direct membership rule to a device collection.

## SYNTAX

### ByCollectionIdAndResourceId (Default)
```
Add-CMDeviceCollectionDirectMembershipRule -CollectionId <String> [-PassThru] -ResourceId <Int32[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdAndResourceValue
```
Add-CMDeviceCollectionDirectMembershipRule -CollectionId <String> [-PassThru] -Resource <IResultObject[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameAndResourceId
```
Add-CMDeviceCollectionDirectMembershipRule -CollectionName <String> [-PassThru] -ResourceId <Int32[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameAndResourceValue
```
Add-CMDeviceCollectionDirectMembershipRule -CollectionName <String> [-PassThru] -Resource <IResultObject[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionValueAndResourceId
```
Add-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> [-PassThru] -ResourceId <Int32[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionValueAndResourceValue
```
Add-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> [-PassThru] -Resource <IResultObject[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add a direct membership rule to a device collection.
A _direct_ membership rule lets you explicitly choose the members of the device collection.
You can't add membership rules to default collections. Any collection that you target should have an ID that starts with the site code, not `SMS`.
For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a direct membership rule

This command adds a direct membership rule to the device collection with ID **XYZ00056**. It adds the resource with ID **16777219** to the collection.

```powershell
Add-CMDeviceCollectionDirectMembershipRule -CollectionId "XYZ00056" -ResourceId 16777219
```

### Example 2: Add a direct membership rule by using the pipeline

This command first uses the **Get-CMCollection** cmdlet to get the collection object named **testCollection**. It then uses the pipeline operator to pass the object to the **Add-CMDeviceCollectionDirectMembershipRule** cmdlet, which adds the direct membership rule to the device collection object. It adds the device with ID **16777219** to the collection.

```powershell
Get-CMCollection -Name "testCollection" | Add-CMDeviceCollectionDirectMembershipRule -ResourceId 16777219
```

## PARAMETERS

### -CollectionId

Specify the ID of the device collection to add the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since you can't add membership rules to default collections, this ID starts with the site code and not `SMS`.

```yaml
Type: String
Parameter Sets: ByCollectionIdAndResourceId, ByCollectionIdAndResourceValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of the device collection to add the rule.

```yaml
Type: String
Parameter Sets: ByCollectionNameAndResourceId, ByCollectionNameAndResourceValue
Aliases:

Required: True
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

### -InputObject

Specify an object for the device collection to add the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: ByCollectionValueAndResourceId, ByCollectionValueAndResourceValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -Resource

Specify an array of resource objects to add to the device collection with this direct membership rule. To get this object, use the [Get-CMResource](Get-CMResource.md) cmdlet, or the [Get-CMDevice](Get-CMDevice.md) cmdlet with the `-Resource` parameter.

```yaml
Type: IResultObject[]
Parameter Sets: ByCollectionIdAndResourceValue, ByCollectionNameAndResourceValue, ByCollectionValueAndResourceValue
Aliases: Resources

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId

Specify an array of IDs of the resources to add to the device collection with this direct membership rule. This value is the **ResourceID** property, for example `16777219`.

```yaml
Type: Int32[]
Parameter Sets: ByCollectionIdAndResourceId, ByCollectionNameAndResourceId, ByCollectionValueAndResourceId
Aliases: ResourceIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

[Get-CMDeviceCollectionDirectMembershipRule](Get-CMDeviceCollectionDirectMembershipRule.md)
[Remove-CMDeviceCollectionDirectMembershipRule](Remove-CMDeviceCollectionDirectMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMResource](Get-CMResource.md)
[Get-CMDevice](Get-CMDevice.md)

[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
