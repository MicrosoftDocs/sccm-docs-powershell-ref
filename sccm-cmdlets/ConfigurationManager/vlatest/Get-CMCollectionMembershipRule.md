---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834238
schema: 2.0.0
ms.assetid: 2CAB36B0-7B87-426A-B2E6-9114D97DFEF9
---

# Get-CMCollectionMembershipRule

## SYNOPSIS

## SYNTAX

### ByName (Default)
```
Get-CMCollectionMembershipRule [-CollectionType <CollectionType>] -CollectionName <String>
 -RuleClassName <String> -ChildSearchCriteria <SmsProviderSearch> [-ExtraArguments <Object>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollectionMembershipRule [-CollectionType <CollectionType>] -CollectionId <String>
 -RuleClassName <String> -ChildSearchCriteria <SmsProviderSearch> [-ExtraArguments <Object>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMCollectionMembershipRule [-CollectionType <CollectionType>] -InputObject <IResultObject>
 -RuleClassName <String> -ChildSearchCriteria <SmsProviderSearch> [-ExtraArguments <Object>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


