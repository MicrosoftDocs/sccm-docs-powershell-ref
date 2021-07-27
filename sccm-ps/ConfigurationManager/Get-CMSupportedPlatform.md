---
description: Get a supported platform.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/04/2020
schema: 2.0.0
title: Get-CMSupportedPlatform
---

# Get-CMSupportedPlatform

## SYNOPSIS

Get a supported platform.

## SYNTAX

```
Get-CMSupportedPlatform [-Fast] [-MaxVersion <String>] [-MinVersion <String>] [-Name <String>]
 [-Platform <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Get a supported platform. Configuration Manager maintains a list of supported platforms, which applies to various objects such as compliance policies, package programs, and task sequences. These objects only apply to devices with the specified platforms.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all Windows 10 platforms by name

```powershell
Get-CMSupportedPlatform -Name "*Windows*10*" -Fast
```

### Example 2: Get all Windows 8 platforms by version

```powershell
Get-CMSupportedPlatform -Fast -MinVersion "6.2*"
```

### Example 3: Get all platforms

This example gets all supported platforms for the site, and only displays the name.

```powershell
Get-CMSupportedPlatform -Fast | Select-Object DisplayText
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

### -MaxVersion

Filter the list of supported platforms by a specific maximum OS version. For example, `"10.00.99999.9999"`.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSMaxVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -MinVersion

Filter the list of supported platforms by a specific maximum OS version. For example, `"10.00.0000.0"`.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSMinVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Name

Filter the list of supported platforms by name. You can specify a specific platform name, for example, `"All Windows 10 (64-bit)"`. You can also use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

For example, `"*Windows*10*"` for all Windows 10 platforms.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DisplayText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Platform

Filter the list of supported platforms by OS platform. For example, `"I386"` or `"x64"`.

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSPlatform

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_SupportedPlatforms
### IResultObject#SMS_SupportedPlatforms
## NOTES

## RELATED LINKS

[Set-CMComplianceSupportedPlatform](Set-CMComplianceSupportedPlatform.md)
