---
author: aczechowski
description: Gets Configuration Manager software metering settings.
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMSoftwareMeteringSetting
titleSuffix: Configuration Manager
---

# Get-CMSoftwareMeteringSetting

## SYNOPSIS
Gets Configuration Manager software metering settings.

## SYNTAX

```
Get-CMSoftwareMeteringSetting [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareMeteringSetting** cmdlet gets a software metering settings object in Microsoft System Center Configuration Manager.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSoftwareMeteringSetting](Set-CMSoftwareMeteringSetting.md)


