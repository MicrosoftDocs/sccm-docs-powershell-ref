---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834258
schema: 2.0.0
ms.assetid: 858C2F49-80B8-4B63-B45D-B3B3324A9371
---

# New-CMAssetIntelligenceCatalogItem

## SYNOPSIS
Creates an item for the Asset Intelligence catalog.

## SYNTAX

```
New-CMAssetIntelligenceCatalogItem -CategoryName <String> [-Description <String>] [-LanguageId <Int32>]
 -Type <Types> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAssetIntelligenceCatalogItem** cmdlet creates software categories, software families, and custom software labels from the Asset Intelligence catalog in Microsoft System Center Configuration Manager.

The Asset Intelligence catalog contains categorization and identification information for software titles.
The catalog includes predefined categories and families.
Predefined items cannot be modified.
In addition to predefined software categories and software families, you can create custom categories and families.
You can also create custom software labels.

## EXAMPLES

### Example 1: Create category label item in the catalog
```
PS C:\>New-CMAssetIntelligenceCatalogItem -CategoryName "Databases" -LanguageId 1033 -Type TypeTag
```

This command creates a category label in the Asset Intelligence catalog named Databases that has a language ID of 1033 and a type of TypeTag.

### Example 2: Create a category item in the catalog
```
PS C:\>New-CMAssetIntelligenceCatalogItem -CategoryName "Database Tools" -Type TypeCategory
```

This command creates a category in the Asset Intelligence catalog named Database Tools that has a type of TypeCategory.

### Example 3: Create a category family in the catalog
```
PS C:\>New-CMAssetIntelligenceCatalogItem -CategoryName "Database Software" -Type TypeFamily
```

This command creates a category family item in the Asset Intelligence catalog family named Database Software that has a type of TypeFamily.

## PARAMETERS

### -CategoryName
Specifies the name of a category, family, or label in the Asset Intelligence catalog.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### -LanguageId
Specifies the locale ID for an item.
For more information and a list of locale IDs, see the Locale IDs Assigned by Microsoft topic at [http://go.microsoft.com/fwlink/?LinkId=262651](http://go.microsoft.com/fwlink/?LinkId=262651).

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

### -Type
Specifies the type of Asset Intelligence catalog item.
The acceptable values for this parameter are:

- TypeCategory
- TypeFamily
- TypeTag

```yaml
Type: Types
Parameter Sets: (All)
Aliases: 
Accepted values: TypeCategory, TypeFamily, TypeTag

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

[Get-CMAssetIntelligenceCatalogItem](./Get-CMAssetIntelligenceCatalogItem.md)

[Remove-CMAssetIntelligenceCatalogItem](./Remove-CMAssetIntelligenceCatalogItem.md)

[Set-CMAssetIntelligenceCatalogItem](./Set-CMAssetIntelligenceCatalogItem.md)


