---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Remove-CMDeviceCollectionIncludeMembershipRule
---

# Remove-CMDeviceCollectionIncludeMembershipRule

## SYNOPSIS

Remove an include membership rule from a device collection.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionName <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionName <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove an include membership rule from a device collection.
An _include_ membership rule includes the members of another collection in the device collections where the rule is applied.

For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

When you remove an include membership rule to a collection, a resource may no longer be a member of the device collection. This action can cause any software or configuration deployment to not apply to a device.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove an include membership rule

This command removes the include membership rule for the **All Systems** collection from the device collection named **Device**.
Specifying the **Force** parameter indicates that the membership rule is removed without prompting you.

```powershell
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionName "Device" -IncludeCollectionName "All Systems" -Force
```

### Example 2: Remove an include membership rule by using the pipeline

This command first uses the **Get-CMCollection** cmdlet to get the device collection object named **Device**. It then uses the pipeline operator to pass the object to the **Remove-CMDeviceCollectionIncludeMembershipRule** cmdlet.

```powershell
Get-CMCollection -Name "Device" | Remove-CMDeviceCollectionIncludeMembershipRule -IncludeCollectionName "All Systems" -Force
```

## PARAMETERS

### -CollectionId

Specify the ID of the device collection to remove the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since default collections don't have include membership rules, this ID starts with the site code and not `SMS`.

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

Specify the name of the device collection to remove the rule.

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

Forces the command to run without asking for user confirmation.

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

### -IncludeCollection

Specify an object for the included collection to remove the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

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

Specify the ID of the included collection to remove the rule. This value is the **CollectionID** property, for example, `XYZ00012`. You can include default collections, so this value can start with either the site code or `SMS`.

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

Specify the name of the included collection to remove the rule.

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

### -InputObject

Specify an object for the device collection to remove the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

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

[Add-CMDeviceCollectionIncludeMembershipRule](Add-CMDeviceCollectionIncludeMembershipRule.md)
[Get-CMDeviceCollectionIncludeMembershipRule](Get-CMDeviceCollectionIncludeMembershipRule.md)

[Remove-CMCollectionIncludeMembershipRule](Remove-CMCollectionIncludeMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Remove-CMUserCollectionIncludeMembershipRule](Remove-CMUserCollectionIncludeMembershipRule.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
