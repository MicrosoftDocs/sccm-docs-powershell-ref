---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
ms.assetid: 55D600D1-7CFB-4F4C-BCAC-81F19FF7B8A3
online version: https://go.microsoft.com/fwlink/?linkid=833651
schema: 2.0.0
---

# Set-CMAssetIntelligenceCatalogItem

## SYNOPSIS
Changes the properties of an item in the Asset Intelligence catalog.

## SYNTAX

### SetById (Default)
```
Set-CMAssetIntelligenceCatalogItem -Id <String> [-NewCategoryName <String>] [-Description <String>]
 [-LanguageId <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMAssetIntelligenceCatalogItem -CategoryName <String> [-NewCategoryName <String>] [-Description <String>]
 [-LanguageId <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMAssetIntelligenceCatalogItem -InputObject <IResultObject> [-NewCategoryName <String>]
 [-Description <String>] [-LanguageId <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAssetIntelligenceCatalogItem** cmdlet changes the properties of software categories, software families, and custom software labels in the Microsoft System Center Configuration Manager Asset Intelligence catalog.

The Asset Intelligence catalog contains categorization and identification information for software titles.
The catalog includes predefined categories and families.
Predefined items cannot be modified.
In addition to predefined software categories and software families, you can create custom categories and families.
You can also create custom software labels.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


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
For more information and a list of locale IDs, see [Locale IDs Assigned by Microsoft](http://go.microsoft.com/fwlink/?LinkId=262651).

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

[Get-CMAssetIntelligenceCatalogItem](Get-CMAssetIntelligenceCatalogItem.md)

[New-CMAssetIntelligenceCatalogItem](New-CMAssetIntelligenceCatalogItem.md)

[Remove-CMAssetIntelligenceCatalogItem](Remove-CMAssetIntelligenceCatalogItem.md)


