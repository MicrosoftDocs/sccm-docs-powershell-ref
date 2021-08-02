---
description: Gets configuration categories in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMCategory
---

# Get-CMCategory

## SYNOPSIS
Gets configuration categories in Configuration Manager.

## SYNTAX

### GetCategoryByName (Default)
```
Get-CMCategory [-CategoryType <CategoryType>] [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### GetCategoryById
```
Get-CMCategory -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCategory** cmdlet gets configuration categories in Configuration Manager.
Configuration categories offer an optional method of sorting and filtering configuration baselines and configuration items in Configuration Manager and Configuration Manager reports.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get configuration categories by using a name
```
PS XYZ:\> Get-CMCategory -CategoryType "DriverCategories" -Name "NewLaptopDriverSet"
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
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_CategoryInstance
### IResultObject#SMS_CategoryInstance
## NOTES

## RELATED LINKS

[New-CMCategory](New-CMCategory.md)

[Remove-CMCategory](Remove-CMCategory.md)


