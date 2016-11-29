---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834291
schema: 2.0.0
ms.assetid: F291D73C-1D80-4D78-AC0C-643BECDF0F33
---

# New-CMCategory

## SYNOPSIS
Creates a configuration category in Configuration Manager.

## SYNTAX

```
New-CMCategory -Name <String> -CategoryType <CategoryType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCategory** cmdlet creates a configuration category in Microsoft System Center Configuration Manager.
Configuration categories offer an optional method of sorting and filtering configuration baselines and configuration items in System Center Configuration Manager and Configuration Manager reports.

## EXAMPLES

### Example 1: Create a configuration category
```
PS C:\>New-CMCategory -CategoryType "DriverCategories" -Name "NewLaptopDriverSet"
```

This command creates a new category in DriverCategories named NewLaptopDriverSet.

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
Parameter Sets: (All)
Aliases: 
Accepted values: AppCategories, BaselineCategories, CatalogCategories, DriverCategories, UserCategories

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

### -Name
Specifies a name for the configuration category.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedCategoryInstanceName

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Remove-CMCategory](./Remove-CMCategory.md)

[Get-CMCategory](./Get-CMCategory.md)


