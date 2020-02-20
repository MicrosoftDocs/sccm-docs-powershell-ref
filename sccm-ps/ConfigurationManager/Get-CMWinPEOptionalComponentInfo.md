---
author: aczechowski
description: Gets WinPE optional component information.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMWinPEOptionalComponentInfo
titleSuffix: Configuration Manager
---

# Get-CMWinPEOptionalComponentInfo

## SYNOPSIS
Gets WinPE optional component information.

## SYNTAX

### SearchByName (Default)
```
Get-CMWinPEOptionalComponentInfo [-Name <String>] -Architecture <String> [-LanguageId <UInt32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMWinPEOptionalComponentInfo -UniqueId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMWinPEOptionalComponentInfo** cmdlet gets Windows PE (Preinstallation Environment) optional component information.

## EXAMPLES

### Example 1: Get WinPE optional component information by name, architecture, and language ID
```
PS ABC:\> Get-CMWinPEOptionalComponentInfo -Name "WinPE-WMI" -Architecture X64 -LanguageId 1033
```

This command gets the information for the Win PE optional component named WinPE-WMI for the x64 architecture and the language ID of 1033.

### Example 2: Get WinPE optional component information by unique ID
```
PS ABC:\> Get-CMWinPEOptionalComponentInfo -UniqueId 52
```

This command gets the information for all WinPE optional components with the unique ID of 52.

## PARAMETERS

### -Architecture
Specifies the architecture of a WinPE optional component.
Valid values are:

- X64
- X86

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:
Accepted values: X64, X86

Required: True
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

### -LanguageId
Specifies the language ID of the boot image.
Provide a locale ID, such as 1033.

```yaml
Type: UInt32
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a WinPE optional component.

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

### -UniqueId
Specifies the unique ID of a WinPE optional component.

```yaml
Type: String
Parameter Sets: SearchById
Aliases:

Required: True
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
