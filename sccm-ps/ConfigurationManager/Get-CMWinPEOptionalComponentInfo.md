---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/01/2021
schema: 2.0.0
title: Get-CMWinPEOptionalComponentInfo
---

# Get-CMWinPEOptionalComponentInfo

## SYNOPSIS

Get a Windows PE optional component.

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

Use this cmdlet to get a Windows PE (WinPE) optional component. Use this object to add it to or remove it from a boot image with the [Set-CMBootImage](Set-CMBootImage.md) cmdlet. For more information, see [Manage boot images - Optional components](/mem/configmgr/osd/get-started/manage-boot-images#optional-components).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get optional components and add to a boot image

This example gets the .NET and PowerShell optional components, and then adds them to a boot image.

```powershell
$netfxOC = Get-CMWinPEOptionalComponentInfo -Architecture 'x64' -Name 'WinPE-NetFX' -LanguageId 1033
$pwshOC = Get-CMWinPEOptionalComponentInfo -Architecture 'x64' -Name 'WinPE-PowerShell' -LanguageId 1033
$OCs = @($netfxOC, $pwshOC)

Set-CMBootImage -Id 'XYZ00556' -AddOptionalComponent $OCs
```

## PARAMETERS

### -Architecture

Specify the architecture of a WinPE optional component.

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

Specify the _language ID_ for the optional component.

This ID is the decimal equivalent of the Windows _language ID_. For example, `1033` is `0x0409` for **English (United States)**, and `2070` is `0x0816` for **Portuguese (Portugal)**. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

Configuration Manager supports 22 languages. For more information, see [Client languages](/mem/configmgr/core/servers/deploy/install/language-packs#client-languages).

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

Specify the name of the WinPE optional component to get.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -UniqueId

Specify the unique ID of the WinPE optional component to get.

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

For more information on this return object and its properties, see [SMS_WinPEOptionalComponentInfo server WMI class](/mem/configmgr/develop/reference/osd/sms_winpeoptionalcomponentinfo-server-wmi-class).

## RELATED LINKS

[Set-CMBootImage](Set-CMBootImage.md)

[Manage boot images - Optional components](/mem/configmgr/osd/get-started/manage-boot-images#optional-components)
