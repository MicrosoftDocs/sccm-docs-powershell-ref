---
description: Adds a direct membership rule to one or more Configuration Manager user collections.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMUserCollectionDirectMembershipRule
---

# Add-CMUserCollectionDirectMembershipRule

## SYNOPSIS
Adds a direct membership rule to one or more Configuration Manager user collections.

## SYNTAX

### ByCollectionValueAndResourceValue (Default)
```
Add-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> [-PassThru] -Resource <IResultObject[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdAndResourceId
```
Add-CMUserCollectionDirectMembershipRule -CollectionId <String> [-PassThru] -ResourceId <Int32[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdAndResourceValue
```
Add-CMUserCollectionDirectMembershipRule -CollectionId <String> [-PassThru] -Resource <IResultObject[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameAndResourceId
```
Add-CMUserCollectionDirectMembershipRule -CollectionName <String> [-PassThru] -ResourceId <Int32[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameAndResourceValue
```
Add-CMUserCollectionDirectMembershipRule -CollectionName <String> [-PassThru] -Resource <IResultObject[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionValueAndResourceId
```
Add-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> [-PassThru] -ResourceId <Int32[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMUserCollectionDirectMembershipRule** cmdlet adds a rule that adds a specific resource to the user collections.
You can specify the user collections by using their names, IDs, or by specifying an object that represents the collections.

A direct rule lets you explicitly choose the members of the user collection.
For more information on collection rules in Configuration Manager, see [Introduction to Collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a direct membership rule to a user collection
```
PS XYZ:\>Add-CMUserCollectionDirectMembershipRule -CollectionName "All Mobile Devices" -ResourceId "Res_94412512"
```

This command adds a direct membership rule that has the ID Res_94412512 to the Configuration Manager user collection named All Mobile Devices.

## PARAMETERS

### -CollectionId
Specifies the ID of the user collection where the rule is applied.

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
Specifies the name of a user collection where the rule is applied.

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
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByCollectionValueAndResourceValue, ByCollectionValueAndResourceId
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
Specifies the type of the resource that the cmdlet adds to the user collections.

```yaml
Type: IResultObject[]
Parameter Sets: ByCollectionValueAndResourceValue, ByCollectionIdAndResourceValue, ByCollectionNameAndResourceValue
Aliases: Resources

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceId
Specifies the ID of a resource that the cmdlet adds to the user collections.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMUserCollection](Get-CMUserCollection.md)

[Get-CMUserCollectionDirectMembershipRule](Get-CMUserCollectionDirectMembershipRule.md)

[Remove-CMUserCollectionDirectMembershipRule](Remove-CMUserCollectionDirectMembershipRule.md)
