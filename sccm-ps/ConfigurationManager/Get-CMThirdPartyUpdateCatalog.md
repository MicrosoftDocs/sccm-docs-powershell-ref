---
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMThirdPartyUpdateCatalog

## SYNOPSIS

Use this cmdlet to get a third-party updates catalog.

## SYNTAX

### SearchByName (Default)
```
Get-CMThirdPartyUpdateCatalog [[-Name] <String>] [-PublisherName <String>] [-SiteCode <String>]
 [-IsSyncEnabled <Boolean>] [-IsCustomCatalog <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMThirdPartyUpdateCatalog [-Id] <String> [-PublisherName <String>] [-SiteCode <String>]
 [-IsSyncEnabled <Boolean>] [-IsCustomCatalog <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1910, use this cmdlet to get a third-party updates catalog.

## EXAMPLES

### Example 1: Get a catalog by ID

This example gets a third-party update catalog by its ID.

```powershell
Get-CMThirdPartyUpdateCatalog -Id $id
```

### Example 2: Get a catalog by name

This example gets a third-party update catalog by its name.

```powershell
Get-CMThirdPartyUpdateCatalog -Name $name
```

### Example 3: Get all catalogs for a site

This example gets all third-party update catalogs for a site by the site code.

```powershell
Get-CMThirdPartyUpdateCatalog -SiteCode $siteCode
```

### Example 4: Get all custom catalogs

This example gets all custom third-party update catalogs.

```powershell
Get-CMThirdPartyUpdateCatalog -IsCustomCatalog $true
```

## PARAMETERS

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

Specify the ID of the catalog.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CatalogId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsCustomCatalog

To filter the results for only custom catalogs, set this parameter to `$true`.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsSyncEnabled

To filter the results for only catalogs that you enable for sync, set this parameter to `$true`.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the catalog.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CatalogName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublisherName

Specify the name of the catalog's publisher.

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

### -SiteCode

Specify the site code to filter the results for a specific site.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_ISVCatalogs

### IResultObject#SMS_ISVCatalogs

## NOTES

## RELATED LINKS
