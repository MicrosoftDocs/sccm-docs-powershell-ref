---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Remove-CMCollectionExcludeMembershipRule
---

# Remove-CMCollectionExcludeMembershipRule

## SYNOPSIS

Remove an exclude membership rule from a device or user collection.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollectionName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollection <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollection <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollectionName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollection <IResultObject>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollectionName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove an exclude membership rule from a device or user collection.
An _exclude_ membership rule excludes the members of another collection from the collections where the rule is applied.

For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

When you remove an exclude membership rule from a collection, resources may become members of the collection. This action can cause any software or configuration deployment to apply to resources in the previously excluded collection.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove an exclude membership rule from a device collection

This command removes the rule that excludes collection **SMSDM001** from the device collection with ID **XYZ00012**.

```powershell
Remove-CMCollectionExcludeMembershipRule -CollectionId "XYZ00012" -ExcludeCollectionId "SMSDM001" -Force
```

## PARAMETERS

### -CollectionId

Specify the ID of the collection to remove the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since default collections don't have exclude membership rules, this ID starts with the site code and not `SMS`.

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

Specify the name of the collection to remove the rule.

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

Specify an object for the excluded collection to remove the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

Specify the ID of the excluded collection to remove the rule. This value is the **CollectionID** property, for example, `XYZ00012`. You can exclude default collections, so this value can start with either the site code or `SMS`.

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Run the command without asking for confirmation.

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

Specify an object for the collection to remove the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
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
Default value: None
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

This cmdlet is similar to **Remove-CMDeviceCollectionExcludeMembershipRule** and **Remove-CMUserCollectionExcludeMembershipRule**, which are specific to the type of collection. This cmdlet works with either device or user collections.

## RELATED LINKS

[Get-CMCollectionExcludeMembershipRule](Get-CMCollectionExcludeMembershipRule.md)

[Remove-CMCollectionDirectMembershipRule](Remove-CMCollectionDirectMembershipRule.md)
[Remove-CMCollectionIncludeMembershipRule](Remove-CMCollectionIncludeMembershipRule.md)
[Remove-CMCollectionQueryMembershipRule](Remove-CMCollectionQueryMembershipRule.md)

[Add-CMDeviceCollectionExcludeMembershipRule](Add-CMDeviceCollectionExcludeMembershipRule.md)
[Add-CMUserCollectionExcludeMembershipRule](Add-CMUserCollectionExcludeMembershipRule.md)

[Get-CMDeviceCollectionExcludeMembershipRule](Get-CMDeviceCollectionExcludeMembershipRule.md)
[Get-CMUserCollectionExcludeMembershipRule](Get-CMUserCollectionExcludeMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
