---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Get-CMThirdPartyUpdateCategory

## SYNOPSIS

Get third-party software update categories.

## SYNTAX

### SearchByName (Default)
```
Get-CMThirdPartyUpdateCategory [[-CatalogName] <String>] [-Id <String>] [-Name <String>] [-ParentId <String>]
 [-PublishOption <PublishOptionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMThirdPartyUpdateCategory [-CatalogId] <String> [-Id <String>] [-Name <String>] [-ParentId <String>]
 [-PublishOption <PublishOptionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMThirdPartyUpdateCategory [-Id <String>] -InputObject <IResultObject> [-Name <String>]
 [-ParentId <String>] [-PublishOption <PublishOptionType>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get third-party software update categories. For more information, see [Enable third-party updates](/mem/configmgr/sum/deploy-use/third-party-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the category for a catalog object

This example gets the category for a third-party update catalog object.

```powershell
Get-CMThirdPartyUpdateCategory -Catalog $catalog
```

### Example 2: Get the category for a catalog and category name

This example gets the category for a specified third-party update catalog name and specified category name.

```powershell
Get-CMThirdPartyUpdateCategory -CatalogName $catalogName -Name $categoryName
```

## PARAMETERS

### -CatalogId

Specify the ID of the third-party update catalog.

```yaml
Type: String
Parameter Sets: SearchById
Aliases:

Required: True
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

Specify the ID of the category.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CategoryId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for a third-party update catalog. To get this object, use the [Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md) cmdlet.

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

Specify the name of the category.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ParentId

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_ISVCatalogCategories
### IResultObject#SMS_ISVCatalogCategories
## NOTES

This cmdlet returns an object of the **SMS_ISVCatalogCategories** WMI class.

## RELATED LINKS

[Set-CMThirdPartyUpdateCategory](Set-CMThirdPartyUpdateCategory.md)

[Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md)
[New-CMThirdPartyUpdateCatalog](New-CMThirdPartyUpdateCatalog.md)
[Remove-CMThirdPartyUpdateCatalog](Remove-CMThirdPartyUpdateCatalog.md)
[Set-CMThirdPartyUpdateCatalog](Set-CMThirdPartyUpdateCatalog.md)

[Publish-CMThirdPartySoftwareUpdateContent](Publish-CMThirdPartySoftwareUpdateContent.md)

[Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates)
