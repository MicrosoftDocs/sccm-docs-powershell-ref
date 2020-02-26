---
description: Creates a conditional access policy.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMConditionalAccessPolicy
---

# New-CMConditionalAccessPolicy

## SYNOPSIS
Creates a conditional access policy.

## SYNTAX

### ByValue (Default)
```
New-CMConditionalAccessPolicy [-DefaultRuleOverride] -TargetedCollection <IResultObject[]>
 [-ExcludedCollection <IResultObject[]>] [-NotificationText <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
New-CMConditionalAccessPolicy [-DefaultRuleOverride] -TargetedCollectionId <String[]>
 [-ExcludedCollectionId <String[]>] [-NotificationText <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
New-CMConditionalAccessPolicy [-DefaultRuleOverride] -TargetedCollectionName <String[]>
 [-ExcludedCollectionName <String[]>] [-NotificationText <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMConditionalAccessPolicy** cmdlet creates a conditional access policy.

NOTE: Ensure that the Administrator has set the notification email address for the Exchange connector before running this cmdlet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a conditional access policy by value
```
PS XYZ:\> New-CMConditionalAccessPolicy -TargetedCollection (Get-CMCollection -Name 'All Users') -DefaultRuleOverride -ExcludedCollection (Get-CMCollection -Name "TestCol") -NotificationText "Succeedtest"
```

This command creates a conditional access policy with a targeted collection named All Users and an excluded collection named TestCol.
The command provides text for the user notification sent by Exchange when the user's device is blocked.

### Example 2: Create a conditional access policy by ID
```
PS XYZ:\> New-CMConditionalAccessPolicy -TargetedCollectionId sms00004 -ExcludedCollectionID TS300014 -NotificationText "Test text" -DefaultRuleOverride
```

This command creates a conditional access policy with a targeted collection with the ID of sms00004 and an excluded collection with the ID TS300014.
The command provides text for the user notification sent by Exchange when the user's device is blocked.

### Example 3: Create a conditional access policy by name
```
PS XYZ:\> New-CMConditionalAccessPolicy -TargetedCollectionName "All Users" -ExcludedCollectionName "TestCol1" -NotificationText "Test text" -DefaultRuleOverride
```

This command creates a conditional access policy with a targeted collection named All Users and an excluded collection named TestCol1.
The command provides text for the user notification sent by Exchange when the user's device is blocked.

## PARAMETERS

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

### -DefaultRuleOverride
Specifies that the devices that are enrolled in Microsoft Intune and compliant with the compliance policies are allowed to access Exchange.
This rule overrides the default Exchange access rule, which means that even if you set the default rule to quarantine or block access, enrolled and compliant devices will still be able to access Exchange.

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
Aliases: ExcludedCollections

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
Aliases: ExcludedCollectionIds

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
Aliases: ExcludedCollectionNames

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

### -NotificationText
Specifies the text of the email that Exchange sends to users when their device is blocked.

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

### -TargetedCollection
Specifies an array of user collection objects.
To obtain a user collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: TargetedCollections

Required: True
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

Required: True
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject#SMS_ConditionAccessManagement

## NOTES

## RELATED LINKS

[Get-CMCollection](Get-CMCollection.md)

[Get-CMConditionalAccessPolicy](Get-CMConditionalAccessPolicy.md)

[Remove-CMConditionalAccessPolicy](Remove-CMConditionalAccessPolicy.md)

[Set-CMConditionalAccessPolicy](Set-CMConditionalAccessPolicy.md)
