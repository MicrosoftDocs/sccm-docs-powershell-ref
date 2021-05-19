---
description: Gets a collection query membership rule.
external help file: AdminUI.PS.psm1-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMCollectionQueryMembershipRule
---

# Get-CMCollectionQueryMembershipRule

## SYNOPSIS
Gets a collection query membership rule.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
