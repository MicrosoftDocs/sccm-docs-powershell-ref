---
description: Gets WinPE optional component information.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Get-CMWinPEOptionalComponentInfo
---

# Get-CMWinPEOptionalComponentInfo

## SYNOPSIS
Gets WinPE optional component information.

## SYNTAX

### SearchByName (Default)
```
Get-CMWinPEOptionalComponentInfo -Architecture <String> [-LanguageId <UInt32>] [-Name <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMWinPEOptionalComponentInfo -UniqueId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMWinPEOptionalComponentInfo** cmdlet gets Windows PE (Preinstallation Environment) optional component information.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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

### None

## OUTPUTS

### IResultObject[]#SMS_WinPEOptionalComponentInfo

### IResultObject#SMS_WinPEOptionalComponentInfo

## NOTES

## RELATED LINKS
