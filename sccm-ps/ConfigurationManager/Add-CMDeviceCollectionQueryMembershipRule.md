---
title: Add-CMDeviceCollectionQueryMembershipRule
titleSuffix: Configuration Manager
description: Adds a query membership rule to one or more Configuration Manager device collections.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Add-CMDeviceCollectionQueryMembershipRule

## SYNOPSIS
Adds a query membership rule to one or more Configuration Manager device collections.

## SYNTAX

### ByCollectionId (Default)
```
Add-CMDeviceCollectionQueryMembershipRule -CollectionId <String> -RuleName <String> -QueryExpression <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionName
```
Add-CMDeviceCollectionQueryMembershipRule -CollectionName <String> -RuleName <String> -QueryExpression <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionValue
```
Add-CMDeviceCollectionQueryMembershipRule -Collection <IResultObject> -RuleName <String>
 -QueryExpression <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDeviceCollectionQueryMembershipRule** cmdlet adds a rule that adds devices to the collections based on a query.
You can specify the device collections by names, IDs, or an object that represents the collections.
The query is specified as a text string.

A query rule lets you dynamically update the members of a collection based on a query that is run on a schedule.
For more information on collection rules in Microsoft System Center Configuration Manager, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Add a query membership rule
```
PS C:\>Add-CMDeviceCollectionQueryMembershipRule -CollectionName "Mobile Windows 7 Devices" -QueryExpression "select SMS_R_System.ResourceId, SMS_R_System.ResourceType, SMS_R_System.Name, SMS_R_System.SMSUniqueIdentifier, SMS_R_System.ResourceDomainORWorkgroup, SMS_R_System.Client from  SMS_R_System inner join SMS_G_System_TPM on SMS_G_System_TPM.ResourceID = SMS_R_System.ResourceId" -RuleName "TPM Information"
```

This command adds a membership rule named TPM Information to the device collection named Mobile Windows 7 Devices.
The *QueryExpression* parameter specifies the query that defines the membership rule.

## PARAMETERS

### -Collection
Specifies a Configuration Manager device collection object.
To obtain a device collection object, use the **Get-CMDeviceCollection** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByCollectionValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of the device collection where the rule is applied.

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
Specifies the name of the device collection where the rule is applied.

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
Specifies the query expression that Configuration Manager uses to update the device collections.

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

[Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433)

[Get-CMDeviceCollectionQueryMembershipRule](Get-CMDeviceCollectionQueryMembershipRule.md)

[Remove-CMDeviceCollectionQueryMembershipRule](Remove-CMDeviceCollectionQueryMembershipRule.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
