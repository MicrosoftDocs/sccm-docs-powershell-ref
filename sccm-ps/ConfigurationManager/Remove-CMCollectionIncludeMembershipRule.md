---
title: Remove-CMCollectionIncludeMembershipRule
titleSuffix: Configuration Manager
description: Removes a collection include membership rule.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Remove-CMCollectionIncludeMembershipRule

## SYNOPSIS
Removes a collection include membership rule.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
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

### -Force
 

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

### -IncludeCollection
 

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

### -IncludeCollectionId
 

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

### -IncludeCollectionName
 

```yaml
Type: String
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
Aliases: 

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

