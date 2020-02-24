---
author: aczechowski
description: Gets an item from the Asset Intelligence catalog.
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMAssetIntelligenceCatalogItem
titleSuffix: Configuration Manager
---

# Get-CMAssetIntelligenceCatalogItem

## SYNOPSIS
Gets an item from the Asset Intelligence catalog.

## SYNTAX

### SearchByName (Default)
```
Get-CMAssetIntelligenceCatalogItem [-CategoryName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAssetIntelligenceCatalogItem -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAssetIntelligenceCatalogItem** cmdlet gets software categories, software families, and custom software labels from the Asset Intelligence catalog in Microsoft System Center Configuration Manager.

The Asset Intelligence catalog contains categorization and identification information for software titles.
The catalog includes predefined categories and families.
Predefined items cannot be modified.
In addition to predefined software categories and software families, you can create custom categories and families.
You can also create custom software labels.

For more information about the Asset Intelligence catalog, see [Introduction to Asset Intelligence in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg681998(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get catalog items by category name
```
PS XYZ:\> Get-CMAssetIntelligenceCatalogItem -CategoryName "Browsers"
```

This command gets Asset Intelligence catalog items by category name.

### Example 2: Get catalog items by category ID
```
PS XYZ:\> Get-CMAssetIntelligenceCatalogItem -Id "1211"
```

This command gets Asset Intelligence catalog items by category ID.

## PARAMETERS

### -CategoryName
Specifies the name of a category, family, or label in the Asset Intelligence catalog.

```yaml
Type: String
Parameter Sets: SearchByName
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
Parameter Sets: SearchByIdMandatory
Aliases: CategoryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMAssetIntelligenceCatalogItem](New-CMAssetIntelligenceCatalogItem.md)

[Remove-CMAssetIntelligenceCatalogItem](Remove-CMAssetIntelligenceCatalogItem.md)

[Set-CMAssetIntelligenceCatalogItem](Set-CMAssetIntelligenceCatalogItem.md)


