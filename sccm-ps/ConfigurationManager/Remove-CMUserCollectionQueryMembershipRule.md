<<<<<<< HEAD
---
title: Remove-CMUserCollectionQueryMembershipRule
titleSuffix: Configuration Manager
description: Removes a query membership rule from one or more user collection in the Configuration Manager hierarchy.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Collections-help.xml
ms.assetid: EE51B872-1986-4551-B4C0-7E92529AA20C
online version: https://go.microsoft.com/fwlink/?linkid=834277
schema: 2.0.0
>>>>>>> master
---

# Remove-CMUserCollectionQueryMembershipRule

## SYNOPSIS
Removes a query membership rule from one or more user collection in the Configuration Manager hierarchy.

## SYNTAX

### ByValue (Default)
```
Remove-CMUserCollectionQueryMembershipRule -InputObject <IResultObject> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMUserCollectionQueryMembershipRule -CollectionName <String> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMUserCollectionQueryMembershipRule -CollectionId <String> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMUserCollectionQueryMembershipRule** cmdlet removes a query rule from the specified user collections.
You can specify the user collections by using their names, IDs, or by specifying an input object that represents the collections.

For more information about membership rules in Microsoft System Center Configuration Manager, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove a rule from a collection by using the collection name
```
PS XYZ:\> Remove-CMUserCollectionQueryMembershipRule -CollectionName "Remote Users" -RuleName "Remote Users by Domain"
```

This command removes the rule named Remote Users by Domain from the collection named Remote Users.

## PARAMETERS

### -CollectionId
```yaml
Type: String
Parameter Sets: ById
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
Parameter Sets: ByName
Aliases: Name

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
Parameter Sets: ByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RuleName
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMUserCollectionQueryMembershipRule](Add-CMUserCollectionQueryMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Get-CMUserCollectionQueryMembershipRule](Get-CMUserCollectionQueryMembershipRule.md)


