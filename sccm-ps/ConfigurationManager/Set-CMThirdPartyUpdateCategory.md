---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Set-CMThirdPartyUpdateCategory

## SYNOPSIS

Modify third-party software update categories.

## SYNTAX

### SearchByName (Default)
```
Set-CMThirdPartyUpdateCategory [[-CatalogName] <String>] [-EnableCategory <Boolean>] [-Id <String>]
 [-Name <String>] [-ParentId <String>] [-PassThru] [-PublishOption <PublishOptionType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Set-CMThirdPartyUpdateCategory [[-CatalogId] <String>] [-EnableCategory <Boolean>] [-Id <String>]
 [-Name <String>] [-ParentId <String>] [-PassThru] [-PublishOption <PublishOptionType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByCategory
```
Set-CMThirdPartyUpdateCategory [-Category] <IResultObject[]> [-EnableCategory <Boolean>] [-PassThru]
 [-PublishOption <PublishOptionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValue
```
Set-CMThirdPartyUpdateCategory [-EnableCategory <Boolean>] [-Id <String>] -InputObject <IResultObject>
 [-Name <String>] [-ParentId <String>] [-PassThru] [-PublishOption <PublishOptionType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to modify third-party software update categories. For more information, see [Enable third-party updates](/mem/configmgr/sum/deploy-use/third-party-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Set-CMThirdPartyUpdateCategory -Catalog $catalog -Id $categoryId -PublishOption $publishOption -EnableCategories $true
$catalog | Set-CMThirdPartyUpdateCategory -Name $categoryName -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -CatalogId $catalogId -ParentId $parentId -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -CatalogName $catalogName -Name $categoryName -ParentId $parentId -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -Categories $categories -PublishOption $publishOption -EnableCategories $true
```

## PARAMETERS

### -CatalogId

Specify the ID of the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchById
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CatalogName

Specify the name of the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Category

Specify an object for the the third-party update catalog category.

```yaml
Type: IResultObject[]
Parameter Sets: SearchByCategory
Aliases: Categories

Required: True
Position: 0
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

### -EnableCategory

Enable the catagory for the third-party update catalog.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

Specify the category ID for the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchByName, SearchById, SearchByValue
Aliases: CategoryId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for the third-party update catalog. To get this object, use the [Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Catalog

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the category name for the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchByName, SearchById, SearchByValue
Aliases: CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ParentId

Specify the parent ID of the the third-party update catalog category.

```yaml
Type: String
Parameter Sets: SearchByName, SearchById, SearchByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -PublishOption

```yaml
Type: PublishOptionType
Parameter Sets: (All)
Aliases:
Accepted values: Skip, MetadataOnly, FullContent

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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_ISVCatalogCategories
## NOTES

This cmdlet returns an object of the **SMS_ISVCatalogCategories** WMI class.

## RELATED LINKS

[Get-CMThirdPartyUpdateCategory](Get-CMThirdPartyUpdateCategory.md)

[Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md)
[New-CMThirdPartyUpdateCatalog](New-CMThirdPartyUpdateCatalog.md)
[Remove-CMThirdPartyUpdateCatalog](Remove-CMThirdPartyUpdateCatalog.md)
[Set-CMThirdPartyUpdateCatalog](Set-CMThirdPartyUpdateCatalog.md)

[Publish-CMThirdPartySoftwareUpdateContent](Publish-CMThirdPartySoftwareUpdateContent.md)

[Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates)
