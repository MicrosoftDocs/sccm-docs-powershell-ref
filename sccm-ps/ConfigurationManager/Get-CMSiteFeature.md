---
description: Get an optional feature.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/26/2021
schema: 2.0.0
title: Get-CMSiteFeature
---

# Get-CMSiteFeature

## SYNOPSIS

Get an optional feature.

## SYNTAX

```
Get-CMSiteFeature [-Fast] [-Name <String>] [-Prerelease] [-Production] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get optional features for the site. For more information, see [Enable optional features from updates](/mem/configmgr/core/servers/manage/install-in-console-updates#bkmk_options).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all pre-release features

This example gets all pre-release features for the site, without loading lazy properties.

```powershell
Get-CMSiteFeature -Prerelease -Fast
```

### Example 2: Get a specific feature

This example gets details for the feature named **Task Sequence Debugger**.

```powershell
Get-CMSiteFeature -Name "Task Sequence Debugger"
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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

### -Name

Specify the name of the optional feature to get.

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

### -Prerelease

Add this parameter to filter the results on pre-release features. For more information, see [Pre-release features in Configuration Manager](/mem/configmgr/core/servers/manage/pre-release-features).

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

### -Production

Add this parameter to filter the results to features that aren't optional.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject#SMS_CM_UpdateFeatures
## NOTES

For more information on this return object and its properties, see [SMS_CM_UpdateFeatures server WMI class](/mem/configmgr/develop/reference/sum/sms_cm_updatefeatures-server-wmi-class).

## RELATED LINKS

[Enable-CMSiteFeature](Enable-CMSiteFeature.md)
