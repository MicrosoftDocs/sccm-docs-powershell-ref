---
title: Add-CMUserCollectionQueryMembershipRule
titleSuffix: Configuration Manager
description: Adds a query membership rule to one or more Configuration Manager user collections.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Add-CMUserCollectionQueryMembershipRule

## SYNOPSIS
Adds a query membership rule to one or more Configuration Manager user collections.

## SYNTAX

### ByCollectionValue (Default)
```
Add-CMUserCollectionQueryMembershipRule -Collection <IResultObject> -RuleName <String>
 -QueryExpression <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByCollectionId
```
Add-CMUserCollectionQueryMembershipRule -CollectionId <String> -RuleName <String> -QueryExpression <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionName
```
Add-CMUserCollectionQueryMembershipRule -CollectionName <String> -RuleName <String> -QueryExpression <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMUserCollectionQueryMembershipRule** cmdlet adds a rule that adds users to the collections based on a query in Microsoft System Center Configuration Manager.
You can specify the user collections by using their names, IDs, or by specifying an object that represents the collections.
The query is specified as a text string.

A query rule lets you dynamically update the members of a collection based on a query that is run on a schedule.
For more information on collection rules, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Add a rule to a collection by using a name
```
PS C:\>Add-CMUserCollectionQueryMembershipRule -CollectionName "Remote Users" -QueryExpression "select SMS_R_USER.ResourceID,SMS_R_USER.ResourceType,SMS_R_USER.Name,SMS_R_USER.UniqueUserName,SMS_R_USER.WindowsNTDomain from SMS_R_User" -RuleName "Remote Users by Domain"
```

This command adds a rule named Remote Users by Domain to the collection named Remote Users.
The command specifies the query as a string.

## PARAMETERS

### -Collection
Specifies a Configuration Manager user collection object.
To obtain a user collection object, use the [Get-CMUserCollection](Get-CMUserCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByCollectionValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of the user collection where the rule is applied.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of the user collection where the rule is applied.

```yaml
Type: String
Parameter Sets: ByCollectionName
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
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -QueryExpression
Specifies the query expression that Configuration Manager uses to update the user collections.

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

### -RuleName
Specifies the name for the rule.

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

[Get-CMUserCollection](Get-CMUserCollection.md)

[Get-CMUserCollectionQueryMembershipRule](Get-CMUserCollectionQueryMembershipRule.md)

[Remove-CMUserCollectionQueryMembershipRule](Remove-CMUserCollectionQueryMembershipRule.md)


