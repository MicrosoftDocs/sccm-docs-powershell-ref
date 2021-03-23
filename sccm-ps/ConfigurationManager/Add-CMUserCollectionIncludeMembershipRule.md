---
description: Adds an include membership rule to one or more Configuration Manager user collections.
external help file: AdminUI.PS-help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMUserCollectionIncludeMembershipRule
---

# Add-CMUserCollectionIncludeMembershipRule

## SYNOPSIS
Adds an include membership rule to one or more Configuration Manager user collections.

## SYNTAX

### ByNameAndName (Default)
```
Add-CMUserCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionName <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Add-CMUserCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Add-CMUserCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Add-CMUserCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Add-CMUserCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Add-CMUserCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionName <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Add-CMUserCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Add-CMUserCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Add-CMUserCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionName <String>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMUserCollectionIncludeMembershipRule** cmdlet adds a rule that includes the members of another collection in the user collections where the rule is applied.
You can specify the user collections where the rule is applied by using their names, IDs, or by specifying an object that represents the collections.
You can specify the collection whose members are included by using its name, ID, or an object that represents the collection.

Configuration Manager dynamically updates the membership of the user collection on a schedule if the membership of the included collection changes.
For more information on these rules, see [Introduction to Collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add an include membership rule to a user collection
```
PS XYZ:\>Add-CMUserCollectionIncludeMembershipRule -CollectionId "9990000D" -IncludeCollectionId "SMSDM001"
```

This command adds an include membership rule that has the ID SMSDM001 to the Configuration Manager user collection that has the ID 9990000D.

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

### -IncludeCollection
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
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

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

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMUserCollection](Get-CMUserCollection.md)

[Get-CMUserCollectionIncludeMembershipRule](Get-CMUserCollectionIncludeMembershipRule.md)

[Remove-CMUserCollectionIncludeMembershipRule](Remove-CMUserCollectionIncludeMembershipRule.md)
