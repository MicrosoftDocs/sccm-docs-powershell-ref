---
description: Gets Asset Intelligence synchronization points.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMAssetIntelligenceSynchronizationPoint
---

# Get-CMAssetIntelligenceSynchronizationPoint

## SYNOPSIS
Gets Asset Intelligence synchronization points.

## SYNTAX

### SearchByName (Default)
```
Get-CMAssetIntelligenceSynchronizationPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-AllSite]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMAssetIntelligenceSynchronizationPoint [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAssetIntelligenceSynchronizationPoint** cmdlet gets one or more Asset Intelligence synchronization points.
Microsoft System Center Configuration Manager uses the Asset Intelligence synchronization point site system role to connect System Center Configuration Manager sites to System Center Online to synchronize Asset Intelligence catalog information.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get an Asset Intelligence synchronization point
```
PS XYZ:\> Get-CMAssetIntelligenceSynchronizationPoint
```

This command gets an Asset Intelligence synchronization point.

## PARAMETERS

### -AllSite
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AllSites

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

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
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

### -SiteSystemServerName
```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName

Required: False
Position: 0
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

[Add-CMAssetIntelligenceSynchronizationPoint](Add-CMAssetIntelligenceSynchronizationPoint.md)

[Remove-CMAssetIntelligenceSynchronizationPoint](Remove-CMAssetIntelligenceSynchronizationPoint.md)

[Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md)


