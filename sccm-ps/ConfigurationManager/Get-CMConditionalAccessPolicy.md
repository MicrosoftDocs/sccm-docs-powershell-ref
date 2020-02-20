---
author: aczechowski
description: Gets a conditional access policy.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMConditionalAccessPolicy
titleSuffix: Configuration Manager
---

# Get-CMConditionalAccessPolicy

## SYNOPSIS
Gets a conditional access policy.

## SYNTAX

### ByValue (Default)
```
Get-CMConditionalAccessPolicy [-TargetedCollection <IResultObject[]>] [-ExcludedCollection <IResultObject[]>]
 [-DefaultRuleOverride <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
Get-CMConditionalAccessPolicy [-TargetedCollectionName <String[]>] [-ExcludedCollectionName <String[]>]
 [-DefaultRuleOverride <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMConditionalAccessPolicy [-TargetedCollectionId <String[]>] [-ExcludedCollectionId <String[]>]
 [-DefaultRuleOverride <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConditionalAccessPolicy** cmdlet gets a conditional access policy.

## EXAMPLES

### Example 1: Get a conditional access policy by name
```
PS XYZ:\> Get-CMConditionalAccessPolicy -TargetedCollection (Get-CMCollection -Name "All Users")
```

This command gets the conditional access policy for the targeted collection named All Users.

### Example 2: Get a conditional access policy by ID
```
PS XYZ:\> Get-CMConditionalAccessPolicy -TargetedCollectionID SMS00002
```

This command gets the conditional access policy for the target collection with the ID of SMS00002.

## PARAMETERS

### -DefaultRuleOverride
Specifies that the devices that are enrolled in Microsoft Intune and compliant with the compliance policies are allowed to access Exchange.
This rule overrides the default Exchange access rule, which means that even if you set the default rule to quarantine or block access, enrolled and compliant devices will still be able to access Exchange.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
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

### -ExcludedCollection
Specifies an array of user collection objects.
To obtain a user collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: ExecludedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedCollectionId
Specifies an array of user collection IDs.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: String[]
Parameter Sets: ById
Aliases: ExecludedCollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedCollectionName
Specifies an array of user collection names.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: ExecludedCollectionNames

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

### -TargetedCollection
Specifies an array of user collection objects.
To obtain a user collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: TargetedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetedCollectionId
Specifies an array of user collection IDs.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: ById
Aliases: TargetedCollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetedCollectionName
Specifies an array of user collection names.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: TargetedCollectionNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCollection](Get-CMCollection.md)

[New-CMConditionalAccessPolicy](New-CMConditionalAccessPolicy.md)

[Remove-CMConditionalAccessPolicy](Remove-CMConditionalAccessPolicy.md)

[Set-CMConditionalAccessPolicy](Set-CMConditionalAccessPolicy.md)


