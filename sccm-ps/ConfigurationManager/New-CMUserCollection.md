---
description: Creates a collection for users and adds the collection to the Configuration Manager hierarchy.
external help file: AdminUI.PS.Collections-help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMUserCollection
---

# New-CMUserCollection

## SYNOPSIS
Creates a collection for users and adds the collection to the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
New-CMUserCollection [-Comment <String>] -LimitingCollectionName <String> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
New-CMUserCollection [-Comment <String>] -InputObject <IResultObject> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
New-CMUserCollection [-Comment <String>] -LimitingCollectionId <String> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMUserCollection** cmdlet creates a collection based on a specific limiting collection.
The limiting collection determines which users can be a member of the user collection that you create.
For example, when you use the All Users collection as the limiting collection, the new collection can include any user in the Configuration Manager hierarchy.
You specify the limiting collection by providing its name or ID.

Users are added to the collection by membership rules.
To add members to the user collection use one of the following membership rule cmdlets:

- Add-CMDeviceCollectionQueryMembershipRule
- Add-CMUserCollectionDirectMembershipRule
- Add-CMUserCollectionExcludeMembershipRule
- Add-CMUserCollectionIncludeMembershipRule

Collections represent logical groupings of resources, such as users and devices.
For more information about Configuration Manager collections, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a user collection
```
PS XYZ:\> New-CMUserCollection -Name "Sales" -LimitingCollectionName "All Users"
```

This command creates a collection for all users in the Sales department.
Specifying All Users for the *LimitingCollectionName* parameter indicates that the new collection can include any user in the Configuration Manager hierarchy.

## PARAMETERS

### -Comment
```yaml
Type: String
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
Parameter Sets: ByValue
Aliases: LimitingCollection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LimitingCollectionId
```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitingCollectionName
```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshSchedule
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshType
```yaml
Type: CollectionRefreshType
Parameter Sets: (All)
Aliases:
Accepted values: None, Manual, Periodic, Continuous, Both

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMDeviceCollectionQueryMembershipRule](Add-CMDeviceCollectionQueryMembershipRule.md)

[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)

[Add-CMUserCollectionExcludeMembershipRule](Add-CMUserCollectionExcludeMembershipRule.md)

[Add-CMUserCollectionIncludeMembershipRule](Add-CMUserCollectionIncludeMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)


