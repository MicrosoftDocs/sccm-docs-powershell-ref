---
description: Synchronizes the Asset Intelligence catalog with System Center Online.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Sync-CMAssetIntelligenceCatalog
---

# Sync-CMAssetIntelligenceCatalog

## SYNOPSIS
Synchronizes the Asset Intelligence catalog with System Center Online.

## SYNTAX

```
Sync-CMAssetIntelligenceCatalog [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Sync-CMAssetIntelligenceCatalog** cmdlet synchronizes the local Asset Intelligence catalog with System Center Online to retrieve the latest software title categorization.
The Asset Intelligence catalog contains categorization and identification information for software titles.
System Center Online accepts only one manual synchronization request in a 12-hour period.

Configuration Manager updates the asset Intelligence catalog by using the Asset Intelligence synchronization point site system role.
You must install an Asset Intelligence synchronization point site system role before you can synchronize the Asset Intelligence catalog with System Center Online.
You can use the Add-CMAssetIntelligenceSynchronizationPoint cmdlet to install an Asset Intelligence synchronization point site system role.

When you manually request catalog synchronization with System Center Online, it could take 15 minutes or longer to complete the synchronization process with System Center Online.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Update the Asset Intelligence catalog
```
PS XYZ:\> Sync-CMAssetIntelligenceCatalog -SiteCode "CM2" -SiteSystemServerName "Contoso-west02"
```

This command the updates the Asset Intelligence catalog on the Configuration Manager site that has the site code CM2 on the site system server named Contoso-west02.

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

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMAssetIntelligenceSynchronizationPoint](Add-CMAssetIntelligenceSynchronizationPoint.md)

[Get-CMAssetIntelligenceSynchronizationPoint](Get-CMAssetIntelligenceSynchronizationPoint.md)

[Send-CMAssetIntelligenceCatalogUpdateRequest](Send-CMAssetIntelligenceCatalogUpdateRequest.md)

[Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md)


