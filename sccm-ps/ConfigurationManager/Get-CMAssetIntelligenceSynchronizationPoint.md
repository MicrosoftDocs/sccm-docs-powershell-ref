---
description: Gets asset intelligence synchronization points.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: Get-CMAssetIntelligenceSynchronizationPoint
---

# Get-CMAssetIntelligenceSynchronizationPoint

## SYNOPSIS
Gets asset intelligence synchronization points.

## SYNTAX

### SearchByName (Default)
```
Get-CMAssetIntelligenceSynchronizationPoint [-AllSite] [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMAssetIntelligenceSynchronizationPoint [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAssetIntelligenceSynchronizationPoint** cmdlet gets one or more asset intelligence synchronization points. Configuration Manager uses the asset intelligence synchronization point to connect to the Microsoft cloud to synchronize catalog information.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all asset intelligence synchronization points

This command gets all asset intelligence synchronization points in the current site.

```powershell
Get-CMAssetIntelligenceSynchronizationPoint
```

### Example 2: Get a specific server

This command gets the asset intelligence synchronization point on the site server named **CMDIV-WEST04.CORP.CONTOSO.COM**, and saves it as the variable **$aisp**. You can then use that variable with other cmdlets, for example [Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md).

```powershell
$aisp = Get-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "CMDIV-WEST04.CORP.CONTOSO.COM"
```

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

### -InputObject
Specifies the input to this cmdlet. You can use this parameter, or you can pipe the input to this cmdlet.

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
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Add-CMAssetIntelligenceSynchronizationPoint](Add-CMAssetIntelligenceSynchronizationPoint.md)

[Remove-CMAssetIntelligenceSynchronizationPoint](Remove-CMAssetIntelligenceSynchronizationPoint.md)

[Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md)
