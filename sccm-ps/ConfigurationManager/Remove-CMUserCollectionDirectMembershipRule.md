---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Remove-CMUserCollectionDirectMembershipRule
---

# Remove-CMUserCollectionDirectMembershipRule

## SYNOPSIS

Remove a direct membership rule from a user collection.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMUserCollectionDirectMembershipRule -CollectionName <String> -ResourceName <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMUserCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMUserCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMUserCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMUserCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMUserCollectionDirectMembershipRule -CollectionId <String> -ResourceName <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceName <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a direct membership rule from a user collection.
A _direct_ membership rule lets you explicitly choose the members of the user collection.
Default collections don't have direct membership rules. Any collection that you target should have an ID that starts with the site code, not `SMS`.
For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

When you remove a direct membership rule from a collection, the resource may no longer be a member of the collection. This action can cause any software or configuration deployment to not apply to the user.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a direct membership rule from a user collection

This command removes the direct membership rule for the resource with ID **33555693** from the user collection that has the ID **XYZ0001A**.

```powershell
Remove-CMUserCollectionDirectMembershipRule -CollectionID "XYZ0001A" -ResourceId "33555693"
```

## PARAMETERS

### -CollectionId

Specify the ID of the user collection with the direct rule to remove. For example, `"XYZ0003F"`.

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

Specify the name of the user collection with the direct rule to remove.

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

Specify a user collection object with the direct rule to remove. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

Specify an array of resource objects to remove from the user collection. To get this object, use the [Get-CMResource](Get-CMResource.md) or [Get-CMUser](Get-CMUser.md) cmdlets.

```yaml
Type: IResultObject[]
Parameter Sets: ByNameAndValue, ByIdAndValue, ByValueAndValue
Aliases: Resources

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId

Specify an array of resource IDs to remove from the user collection. This value is the **ResourceId** property of the SMS_Resource class. For example, `"33555693"`.

```yaml
Type: String[]
Parameter Sets: ByNameAndId, ByIdAndId, ByValueAndId
Aliases: ResourceIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName

Specify an array of resource names to remove the direct membership rules from the user collection.

```yaml
Type: String[]
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
Aliases: ResourceNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)
[Get-CMUserCollectionDirectMembershipRule](Get-CMUserCollectionDirectMembershipRule.md)

[Remove-CMCollectionDirectMembershipRule](Remove-CMCollectionDirectMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)
[Get-CMResource](Get-CMResource.md)
[Get-CMUser](Get-CMUser.md)

[Remove-CMDeviceCollectionDirectMembershipRule](Remove-CMDeviceCollectionDirectMembershipRule.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
