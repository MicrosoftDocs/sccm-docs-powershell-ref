---
description: Removes a direct membership rule from one or more user collections in the Configuration Manager hierarchy.
external help file: AdminUI.PS.Collections-help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMUserCollectionDirectMembershipRule
---

# Remove-CMUserCollectionDirectMembershipRule

## SYNOPSIS
Removes a direct membership rule from one or more user collections in the Configuration Manager hierarchy.

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
The **Remove-CMUserCollectionDirectMembershipRule** cmdlet removes a direct rule from the specified collections.
You can specify the collections by using their names, IDs, or by specifying an object that represents the collections.

For more information about collection rules in Microsoft System Center Configuration Manager, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove all direct membership rules from a user collection
```
PS XYZ:\> Remove-CMUserCollectionDirectMembershipRule -CollectionID "CM0001A" -ResourceId "12733"
```

This command removes all the direct membership rules of the user collection that has the ID CM0001A.

## PARAMETERS

### -CollectionId
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
```yaml
Type: String[]
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
Aliases: ResourceNames

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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Get-CMUserCollectionDirectMembershipRule](Get-CMUserCollectionDirectMembershipRule.md)

[Remove-CMUserCollectionExcludeMembershipRule](Remove-CMUserCollectionExcludeMembershipRule.md)

[Remove-CMUserCollectionIncludeMembershipRule](Remove-CMUserCollectionIncludeMembershipRule.md)

[Remove-CMUserCollectionQueryMembershipRule](Remove-CMUserCollectionQueryMembershipRule.md)


