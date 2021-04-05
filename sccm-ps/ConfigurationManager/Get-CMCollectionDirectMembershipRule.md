---
description: Gets a collection direct membership rule.
external help file: AdminUI.PS-help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMCollectionDirectMembershipRule
---

# Get-CMCollectionDirectMembershipRule

## SYNOPSIS
Gets a collection direct membership rule.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMCollectionDirectMembershipRule -CollectionName <String> [-ResourceName <String>] [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject> [<CommonParameters>]
```

### ByNameAndId
```
Get-CMCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String> [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject> [<CommonParameters>]
```

### ByIdAndId
```
Get-CMCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String> [<CommonParameters>]
```

### ByIdAndName
```
Get-CMCollectionDirectMembershipRule -CollectionId <String> [-ResourceName <String>] [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String> [<CommonParameters>]
```

### ByValueAndName
```
Get-CMCollectionDirectMembershipRule -InputObject <IResultObject> [-ResourceName <String>] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -CollectionId
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

### -InputObject
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

### -Resource
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

### -ResourceId
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

### -ResourceName
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
