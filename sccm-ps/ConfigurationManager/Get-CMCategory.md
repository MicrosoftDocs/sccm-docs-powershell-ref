---
title: Get-CMCategory
titleSuffix: Configuration Manager
description: Gets configuration categories in Configuration Manager.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMCategory

## SYNOPSIS
Gets configuration categories in Configuration Manager.

## SYNTAX

### GetCategoryByName (Default)
```
Get-CMCategory [-Name <String>] [-CategoryType <CategoryType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### GetCategoryById
```
Get-CMCategory -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCategory** cmdlet gets configuration categories in Microsoft System Center Configuration Manager.
Configuration categories offer an optional method of sorting and filtering configuration baselines and configuration items in System Center Configuration Manager and Configuration Manager reports.

## EXAMPLES

### Example 1: Get configuration categories by using a name
```
PS C:\> Get-CMCategory -CategoryType "DriverCategories" -Name "NewLaptopDriverSet"
```

This command gets configuration driver categories in Configuration Manager that have the name NewLaptopDriverSet.

## PARAMETERS

### -CategoryType
Specifies a category type.
Valid values are: 

- BaselineCategories
- DriverCategories
- AppCategories
- GlobalCondition
- CatalogCategories

```yaml
Type: CategoryType
Parameter Sets: GetCategoryByName
Aliases: 
Accepted values: UserCategories, BaselineCategories, DriverCategories, AppCategories, GlobalCondition, CatalogCategories

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

### -Id
Specifies an array of IDs of configuration categories.

```yaml
Type: String[]
Parameter Sets: GetCategoryById
Aliases: CategoryInstanceUniqueid, CategoryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration categories.

```yaml
Type: String
Parameter Sets: GetCategoryByName
Aliases: LocalizedCategoryInstanceName, CategoryName

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

[New-CMCategory](New-CMCategory.md)

[Remove-CMCategory](Remove-CMCategory.md)


