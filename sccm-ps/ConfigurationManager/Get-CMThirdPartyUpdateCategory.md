---
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMThirdPartyUpdateCategory

## SYNOPSIS

Use this cmdlet to get third-party update categories.

## SYNTAX

### SearchByName (Default)
```
Get-CMThirdPartyUpdateCategory [[-CatalogName] <String>] [-Id <String>] [-Name <String>]
 [-PublishOption <PublishOptionType>] [-ParentId <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMThirdPartyUpdateCategory -InputObject <IResultObject> [-Id <String>] [-Name <String>]
 [-PublishOption <PublishOptionType>] [-ParentId <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMThirdPartyUpdateCategory [-CatalogId] <String> [-Id <String>] [-Name <String>]
 [-PublishOption <PublishOptionType>] [-ParentId <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to get third-party update categories.

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
Accept wildcard characters: False
```

### -DisableWildcardHandling

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

Specify an object for a third-party update catalog.

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
Accept wildcard characters: False
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

## RELATED LINKS
