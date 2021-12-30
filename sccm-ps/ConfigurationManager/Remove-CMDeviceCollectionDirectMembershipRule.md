---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Remove-CMDeviceCollectionDirectMembershipRule
---

# Remove-CMDeviceCollectionDirectMembershipRule

## SYNOPSIS

Remove a direct membership rule from a device collection.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -ResourceName <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -ResourceName <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceName <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a direct membership rule from a device collection.
A _direct_ membership rule lets you explicitly choose the members of the device collection.
Default collections don't have direct membership rules. Any collection that you target should have an ID that starts with the site code, not `SMS`.
For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

When you remove a direct membership rule from a collection, the resource may no longer be a member of the collection. This action can cause any software or configuration deployment to not apply to the device.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a direct membership rule from a device collection

This command removes the direct membership rule for the resource with the ID of **2097152004** from the collection named **Devices 01**. Specifying the **Force** parameter indicates that the user isn't prompted before the rule is removed.

```powershell
Remove-CMDeviceCollectionDirectMembershipRule -CollectionName "Devices 01" -ResourceId "2097152004" -Force
```

## PARAMETERS

### -CollectionId

Specify the ID of a device collection with the direct rule to remove. For example, `"XYZ0003F"`.

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

Specify the name of the device collection with the direct rule to remove.

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

Specify a device collection object with the direct rule to remove. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

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

Specify an array of device objects to remove its direct membership rule from the device collection. To get this object, use the [Get-CMResource](Get-CMResource.md) or [Get-CMDevice](Get-CMDevice.md) cmdlets.

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

Specify an array of resource IDs to remove the direct membership rules from the device collection. This value is the **ResourceId** property of the SMS_Resource class. For example, `"33555693"`.

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

Specify an array of resource names to remove the direct membership rules from the device collection.

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

[Add-CMDeviceCollectionDirectMembershipRule](Add-CMDeviceCollectionDirectMembershipRule.md)
[Get-CMDeviceCollectionDirectMembershipRule](Get-CMDeviceCollectionDirectMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMResource](Get-CMResource.md)
[Get-CMDevice](Get-CMDevice.md)

[Remove-CMCollectionDirectMembershipRule](Remove-CMDeviceCollectionDirectMembershipRule.md)

[Remove-CMUserCollectionDirectMembershipRule](Remove-CMUserCollectionDirectMembershipRule.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
