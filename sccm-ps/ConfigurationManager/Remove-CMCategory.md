---
author: aczechowski
description: Removes a configuration category in Configuration Manager.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Remove-CMCategory
titleSuffix: Configuration Manager
---

# Remove-CMCategory

## SYNOPSIS
Removes a configuration category in Configuration Manager.

## SYNTAX

### ByValue (Default)
```
Remove-CMCategory -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMCategory -Name <String[]> [-Force] [-CategoryType <CategoryType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMCategory -Id <String[]> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByCategory
```
Remove-CMCategory [-Force] -CategoryType <CategoryType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMCategory** cmdlet removes a configuration category in Microsoft System Center Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove a configuration category
```
PS XYZ:\> Remove-CMCategory -CategoryType "DriverCategories" -Force -Name "NewLaptopDriverSet"
```

This command removes the category named NewLaptopDriverSet from DriversCategories without prompting you for confirmation.

## PARAMETERS

### -CategoryType
Specifies a category type.
Valid values are:

- UserCategories
- BaselineCategories
- DriverCategories
- AppCategories
- GlobalCondition
- CatalogCategories

```yaml
Type: CategoryType
Parameter Sets: ByName
Aliases:
Accepted values: UserCategories, BaselineCategories, DriverCategories, AppCategories, GlobalCondition, CatalogCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: CategoryType
Parameter Sets: ByCategory
Aliases:
Accepted values: UserCategories, BaselineCategories, DriverCategories, AppCategories, GlobalCondition, CatalogCategories

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
Default value: False
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

### -Force
Forces the command to run without asking for user confirmation.

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
Parameter Sets: ById
Aliases: CategoryInstanceUniqueid, CategoryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Category

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration categories.

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: LocalizedCategoryInstanceName, CategoryName

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

## NOTES

## RELATED LINKS

[Get-CMCategory](Get-CMCategory.md)

[New-CMCategory](New-CMCategory.md)
