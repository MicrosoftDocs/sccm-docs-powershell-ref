---
description: Changes the properties of an item in the Asset Intelligence catalog.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMAssetIntelligenceCatalogItem
---

# Set-CMAssetIntelligenceCatalogItem

## SYNOPSIS
Changes the properties of an item in the Asset Intelligence catalog.

## SYNTAX

### SetById (Default)
```
Set-CMAssetIntelligenceCatalogItem [-Description <String>] -Id <String> [-LanguageId <Int32>]
 [-NewCategoryName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMAssetIntelligenceCatalogItem -CategoryName <String> [-Description <String>] [-LanguageId <Int32>]
 [-NewCategoryName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMAssetIntelligenceCatalogItem [-Description <String>] -InputObject <IResultObject> [-LanguageId <Int32>]
 [-NewCategoryName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAssetIntelligenceCatalogItem** cmdlet changes the properties of software categories, software families, and custom software labels in the Configuration Manager Asset Intelligence catalog.

The Asset Intelligence catalog contains categorization and identification information for software titles.
The catalog includes predefined categories and families.
Predefined items cannot be modified.
In addition to predefined software categories and software families, you can create custom categories and families.
You can also create custom software labels.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the properties of a catalog item by ID
```
PS XYZ:\> Set-CMAssetIntelligenceCatalogItem -Id "1211" -NewCategoryName "Windows Databases" -Description "Windows-based databases" -LanguageId 1033
```

This command changes the category name, description, and language ID for the Asset Intelligence catalog item that has the category ID 1211.

### Example 2: Change the properties of a catalog item category of items
```
PS XYZ:\> Set-CMAssetIntelligenceCatalogItem -CategoryName "Database Tools" -NewCategoryName "Database Clients" -Description "Database client software" -LanguageId 1033
```

This command changes the category name, description, and language ID for the Asset Intelligence catalog item that has the category name Database Tools.

### Example 3: Rename a category
```
PS XYZ:\> Set-CMAssetIntelligenceCatalogItem -CategoryName "Database Clients" -NewCategoryName "Database Server Tools"
```

This command changes the category name of the Asset Intelligence catalog item that has the category name Database Clients to Database Server Tools.

## PARAMETERS

### -CategoryName
Specifies the name of a category, family, or label in the Asset Intelligence catalog.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies the description of a category, family, or label in the Asset Intelligence catalog.

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
Specifies an array of IDs of asset intelligence catalog items.

```yaml
Type: String
Parameter Sets: SetById
Aliases: CategoryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an Asset Intelligence catalog item.
To get an Asset Intelligence catalog item, use the Get-CMAssetIntelligenceCatalogItem cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LanguageId
Specifies the locale ID for an item.
For more information and a list of locale IDs, see [Appendix A: Product Behavior](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewCategoryName
Specifies a new category name for a category, family, or label in the Asset Intelligence catalog.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMAssetIntelligenceCatalogItem](Get-CMAssetIntelligenceCatalogItem.md)

[New-CMAssetIntelligenceCatalogItem](New-CMAssetIntelligenceCatalogItem.md)

[Remove-CMAssetIntelligenceCatalogItem](Remove-CMAssetIntelligenceCatalogItem.md)


