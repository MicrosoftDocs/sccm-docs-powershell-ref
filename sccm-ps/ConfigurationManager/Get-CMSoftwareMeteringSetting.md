---
description: Gets Configuration Manager software metering settings.
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSoftwareMeteringSetting
---

# Get-CMSoftwareMeteringSetting

## SYNOPSIS
Gets Configuration Manager software metering settings.

## SYNTAX

```
Get-CMSoftwareMeteringSetting [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareMeteringSetting** cmdlet gets a software metering settings object in Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get software metering setting object
```
PS XYZ:\> Get-CMSoftwareMeteringSetting

ClientComponentName : Software Metering Agent
FileType            : 2
Flags               : 1
ItemName            : Software Metering Agent
ItemType            : Client Component
PropLists           :
Props               :
RegMultiStringLists :
SiteCode            : CM1
```

This command gets a software metering setting object.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_SCI_ClientComp

### IResultObject#SMS_SCI_ClientComp

## NOTES

## RELATED LINKS

[Set-CMSoftwareMeteringSetting](Set-CMSoftwareMeteringSetting.md)


