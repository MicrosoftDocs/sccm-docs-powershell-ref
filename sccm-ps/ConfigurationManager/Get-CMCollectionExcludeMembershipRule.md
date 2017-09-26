---
external help file: AdminUI.PS.Collections-help.xml
online version: 
schema: 2.0.0
---

# Get-CMCollectionExcludeMembershipRule

## SYNOPSIS
Gets a collection exclude membership rule

## SYNTAX

### ByNameAndName (Default)
```
Get-CMCollectionExcludeMembershipRule -CollectionName <String> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollectionId <String> [<CommonParameters>]
```

### ByIdAndName
```
Get-CMCollectionExcludeMembershipRule -CollectionId <String> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollectionId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMCollectionExcludeMembershipRule -InputObject <IResultObject> [-ExcludeCollectionName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -CollectionId
{{Fill CollectionId Description}}

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
{{Fill CollectionName Description}}

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

### -ExcludeCollection
{{Fill ExcludeCollection Description}}

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

### -ExcludeCollectionId
{{Fill ExcludeCollectionId Description}}

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

### -ExcludeCollectionName
{{Fill ExcludeCollectionName Description}}

```yaml
Type: String
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{Fill InputObject Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

