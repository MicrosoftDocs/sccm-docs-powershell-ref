---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Get-CMThirdPartyUpdateCatalog

## SYNOPSIS

Get a third-party updates catalog.

## SYNTAX

### SearchByName (Default)
```
Get-CMThirdPartyUpdateCatalog [-IsCustomCatalog <Boolean>] [-IsSyncEnabled <Boolean>] [[-Name] <String>]
 [-PublisherName <String>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMThirdPartyUpdateCatalog [-Id] <String> [-IsCustomCatalog <Boolean>] [-IsSyncEnabled <Boolean>]
 [-PublisherName <String>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a third-party updates catalog. For more information, see [Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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

Specify the ID of the catalog. The format is a standard GUID.

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
Accept wildcard characters: True
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
Accept wildcard characters: True
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

This cmdlet returns the **SMS_ISVCatalogs** WMI class object.

## RELATED LINKS

[New-CMThirdPartyUpdateCatalog](New-CMThirdPartyUpdateCatalog.md)
[Remove-CMThirdPartyUpdateCatalog](Remove-CMThirdPartyUpdateCatalog.md)
[Set-CMThirdPartyUpdateCatalog](Set-CMThirdPartyUpdateCatalog.md)

[Publish-CMThirdPartySoftwareUpdateContent](Publish-CMThirdPartySoftwareUpdateContent.md)

[Get-CMThirdPartyUpdateCategory](Get-CMThirdPartyUpdateCategory.md)
[Set-CMThirdPartyUpdateCategory](Set-CMThirdPartyUpdateCategory.md)

[Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates)
