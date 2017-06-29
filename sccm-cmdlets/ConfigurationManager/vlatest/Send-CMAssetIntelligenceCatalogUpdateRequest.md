---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
ms.assetid: F407970C-75BC-43D7-B7A9-E7D44EF71ED7
online version: https://go.microsoft.com/fwlink/?linkid=833593
schema: 2.0.0
---

# Send-CMAssetIntelligenceCatalogUpdateRequest

## SYNOPSIS
Requests a catalog update for uncategorized software titles.

## SYNTAX

### SearchByNameMandatory (Default)
```
Send-CMAssetIntelligenceCatalogUpdateRequest -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Send-CMAssetIntelligenceCatalogUpdateRequest -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Send-CMAssetIntelligenceCatalogUpdateRequest** cmdlet requests an update of the Asset Intelligence catalog for software title categorization from System Center Online.
You can request an update for catalog items or software categories in the Asset Intelligence catalog.

You can also use the Sync-CMAssetIntelligenceCatalog cmdlet to synchronize the local Asset Intelligence catalog with System Center Online to get the latest software title categorization.

## EXAMPLES

### Example 1: Request an update for a software category
```
PS C:\> Send-CMAssetIntelligenceCatalogUpdateRequest -Name "Browsers"
```

This command requests an update of the Asset Intelligence catalog for the software category named Browsers.

## PARAMETERS

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
Specifies an array of IDs of Asset Intelligence catalog items.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: SoftwareKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software categories in the Asset Intelligence catalog.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: CommonName

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

[Sync-CMAssetIntelligenceCatalog](./Sync-CMAssetIntelligenceCatalog.md)


