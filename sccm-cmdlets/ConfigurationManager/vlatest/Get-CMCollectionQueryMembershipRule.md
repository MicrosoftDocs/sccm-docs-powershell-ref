---
external help file: AdminUI.PS.Collections-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834242
schema: 2.0.0
ms.assetid: 2590D2AF-07A2-4E19-B7D4-A12016AF5761
---

# Get-CMCollectionQueryMembershipRule

## SYNOPSIS

## SYNTAX

### ByName (Default)
```
Get-CMCollectionQueryMembershipRule -CollectionName <String> [-RuleName <String>] [<CommonParameters>]
```

### ById
```
Get-CMCollectionQueryMembershipRule -CollectionId <String> [-RuleName <String>] [<CommonParameters>]
```

### ByValue
```
Get-CMCollectionQueryMembershipRule -InputObject <IResultObject> [-RuleName <String>] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

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

### -InputObject
{{Fill InputObject Description}}

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

Required: False
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


