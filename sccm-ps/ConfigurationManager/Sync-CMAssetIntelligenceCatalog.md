---
author: aczechowski
description: Synchronizes the Asset Intelligence catalog with System Center Online.
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Sync-CMAssetIntelligenceCatalog
titleSuffix: Configuration Manager
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

Microsoft System Center Configuration Manager updates the asset Intelligence catalog by using the Asset Intelligence synchronization point site system role.
You must install an Asset Intelligence synchronization point site system role before you can synchronize the Asset Intelligence catalog with System Center Online.
You can use the Add-CMAssetIntelligenceSynchronizationPoint cmdlet to install an Asset Intelligence synchronization point site system role.

When you manually request catalog synchronization with System Center Online, it could take 15 minutes or longer to complete the synchronization process with System Center Online.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Update the Asset Intelligence catalog
```
PS XYZ:\> Sync-CMAssetIntelligenceCatalog -SiteCode "CM2" -SiteSystemServerName "Contoso-west02"
```

This command the updates the Asset Intelligence catalog on the System Center Configuration Manager site that has the site code CM2 on the site system server named Contoso-west02.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMAssetIntelligenceSynchronizationPoint](Add-CMAssetIntelligenceSynchronizationPoint.md)

[Get-CMAssetIntelligenceSynchronizationPoint](Get-CMAssetIntelligenceSynchronizationPoint.md)

[Send-CMAssetIntelligenceCatalogUpdateRequest](Send-CMAssetIntelligenceCatalogUpdateRequest.md)

[Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md)


