---
description: Gets an email notification components.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMEmailNotificationComponent
---

# Get-CMEmailNotificationComponent

## SYNOPSIS
Gets an email notification components.

## SYNTAX

```
Get-CMEmailNotificationComponent [-SiteCode <String>] [-SiteSystemServerName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEmailNotificationComponent** cmdlet gets one or more email notification components Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an email notification component by using a site code
```
PS XYZ:\> Get-CMEmailNotificationComponent -SiteCode "CM2"
```

This command gets a notification component for the site that has the site code CM2.

### Example 2: Get an email notification component by using a site system server name
```
PS XYZ:\> Get-CMEmailNotificationComponent -SiteSystemServerName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM"
```

This command gets a notification component for the site that has the server that has the specified name.

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
Specifies the three-letter site code of the Configuration Manager site that hosts the site system role.

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
Specifies an array of fully qualified domain names (FQDN) of the servers that host the site system role.

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

[Set-CMEmailNotificationComponent](Set-CMEmailNotificationComponent.md)


