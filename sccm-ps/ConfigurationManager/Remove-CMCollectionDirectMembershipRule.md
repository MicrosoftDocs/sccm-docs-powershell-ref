---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Remove-CMCollectionDirectMembershipRule
---

# Remove-CMCollectionDirectMembershipRule

## SYNOPSIS

Remove a direct membership rule from a device or user collection.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMCollectionDirectMembershipRule -CollectionName <String> -ResourceName <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMCollectionDirectMembershipRule -CollectionId <String> -ResourceName <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String[]> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceName <String[]> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a direct membership rule from a device or user collection.
A _direct_ membership rule lets you explicitly choose the members of the collection.
Default collections don't have direct membership rules. Any collection that you target should have an ID that starts with the site code, not `SMS`.
For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

When you remove a direct membership rule from a collection, the resource may no longer be a member of the collection. This action can cause any software or configuration deployment to not apply to the resource.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove the local machine from a collection of test devices

This example uses the Windows environment variable **ComputerName** to remove it from the collection named **Test Devices**. It uses the **Force** parameter to not prompt for confirmation.

```powershell
Remove-CMCollectionDirectMembershipRule -CollectionName 'Test Devices' -ResourceName $env:ComputerName -Force
```

## PARAMETERS

### -CollectionId

Specify the ID of the collection with the direct rule to remove. For example, `"XYZ0003F"`.

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

Specify the name of the collection with the direct rule to remove.

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

Specify a collection object with the direct rule to remove. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

Specify an array of resource objects to remove from the collection. To get this object, use the [Get-CMResource](Get-CMResource.md), [Get-CMDevice](Get-CMDevice.md), or [Get-CMUser](Get-CMUser.md) cmdlets.

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

Specify an array of resource IDs to remove from the collection. This value is the **ResourceId** property of the SMS_Resource class. For example, `"33555693"`.

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

Specify an array of resource names to remove from the collection.

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

This cmdlet is similar to **Remove-CMDeviceCollectionDirectMembershipRule** and **Remove-CMUserCollectionDirectMembershipRule**, which are specific to the type of collection. This cmdlet works with either device or user collections.

## RELATED LINKS

[Get-CMCollectionDirectMembershipRule](Get-CMCollectionDirectMembershipRule.md)

[Remove-CMCollectionExcludeMembershipRule](Remove-CMCollectionExcludeMembershipRule.md)
[Remove-CMCollectionIncludeMembershipRule](Remove-CMCollectionIncludeMembershipRule.md)
[Remove-CMCollectionQueryMembershipRule](Remove-CMCollectionQueryMembershipRule.md)

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
