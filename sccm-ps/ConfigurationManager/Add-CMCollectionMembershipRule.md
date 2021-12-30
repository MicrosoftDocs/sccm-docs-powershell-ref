---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Add-CMCollectionMembershipRule
---

# Add-CMCollectionMembershipRule

## SYNOPSIS

_For system use only_ to add membership rules to collections.

## SYNTAX

### ByName (Default)
```
Add-CMCollectionMembershipRule -ChildSearchCriteria <SmsProviderSearch> -CollectionName <String>
 -CollectionType <CollectionType> [-ExtraArguments <Object>] [-PassThru] -RuleClassName <String>
 -RulePropertyName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Add-CMCollectionMembershipRule -ChildSearchCriteria <SmsProviderSearch> -CollectionId <String>
 -CollectionType <CollectionType> [-ExtraArguments <Object>] [-PassThru] -RuleClassName <String>
 -RulePropertyName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
Add-CMCollectionMembershipRule -ChildSearchCriteria <SmsProviderSearch> -CollectionType <CollectionType>
 [-ExtraArguments <Object>] -InputObject <IResultObject> [-PassThru] -RuleClassName <String>
 -RulePropertyName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet is used by other cmdlets to create membership rules. Don't directly use this cmdlet. Use one of the following cmdlets:

- [Add-CMDeviceCollectionDirectMembershipRule](Add-CMDeviceCollectionDirectMembershipRule.md)
- [Add-CMDeviceCollectionExcludeMembershipRule](Add-CMDeviceCollectionExcludeMembershipRule.md)
- [Add-CMDeviceCollectionIncludeMembershipRule](Add-CMDeviceCollectionIncludeMembershipRule.md)
- [Add-CMDeviceCollectionQueryMembershipRule](Add-CMDeviceCollectionQueryMembershipRule.md)

- [Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)
- [Add-CMUserCollectionExcludeMembershipRule](Add-CMUserCollectionExcludeMembershipRule.md)
- [Add-CMUserCollectionIncludeMembershipRule](Add-CMUserCollectionIncludeMembershipRule.md)
- [Add-CMUserCollectionQueryMembershipRule](Add-CMUserCollectionQueryMembershipRule.md)

## EXAMPLES

## PARAMETERS

### -ChildSearchCriteria
```yaml
Type: SmsProviderSearch
Parameter Sets: (All)
Aliases: SearchCriteria

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
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

### -CollectionName
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

### -CollectionType
```yaml
Type: CollectionType
Parameter Sets: (All)
Aliases:
Accepted values: User, Device

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

### -ExtraArguments
```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -RuleClassName
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

### -RulePropertyName
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

### System.Object
### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
