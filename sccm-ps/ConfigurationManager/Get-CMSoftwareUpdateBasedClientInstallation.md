---
description: Gets a client installation on a Configuration Manager software update point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSoftwareUpdateBasedClientInstallation
---

# Get-CMSoftwareUpdateBasedClientInstallation

## SYNOPSIS
Gets a client installation on a Configuration Manager software update point.

## SYNTAX

```
Get-CMSoftwareUpdateBasedClientInstallation [-SiteCode <String>] [-SiteSystemServerName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateBasedClientInstallation** cmdlet gets a client installation hosted on a software update point for Configuration Manager.

Configuration Manager publishes the Configuration Manager client to a software update point.
This site system role can install the client on computers that do not already have it or upgrade existing clients.

To use software update point based installation, you must use the same Windows Server Update Services (WSUS) server for both client installation and software updates.
This server must be the active software update point in a primary site.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a client installation
```
PS XYZ:\> Get-CMSoftwareUpdateBasedClientInstallation -SiteCode "CM1"
```

This command gets the client installation for the site that has the site code CM1.

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

### -SiteCode
Specifies a site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies an array of names of servers that host a software update point role.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### IResultObject[]#SMS_SCI_Component
### IResultObject#SMS_SCI_Component
## NOTES

## RELATED LINKS

[Set-CMSoftwareUpdateBasedClientInstallation](Set-CMSoftwareUpdateBasedClientInstallation.md)


