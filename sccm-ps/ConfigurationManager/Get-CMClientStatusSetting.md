---
description: Gets client status settings.
external help file: AdminUI.PS.ClientStatus.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMClientStatusSetting
---

# Get-CMClientStatusSetting

## SYNOPSIS
Gets client status settings.

## SYNTAX

```
Get-CMClientStatusSetting [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientStatusSetting** cmdlet gets client status settings for the local computer.
These settings determine the data collection intervals for individual client monitoring activities.

For more information about client settings, see [About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get client status settings for the local computer
```
PS XYZ:\> Get-CMClientStatusSetting
ADRetrieving Schedule  :
CleanUpInterval        : 7
DDRInactiveInterval    : 3
HWInactiveInterval     : 4
NeedADLastLogonTime    :
PolicyInactiveInterval : 3
SettingsID             : 1
StatusInactiveInterval : 6
SWInactiveInterval     : 5
```

This command gets client status settings for the local computer.

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

### IResultObject[]#SMS_CH_Settings

### IResultObject#SMS_CH_Settings

## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings)

[Set-CMClientStatusSetting](Set-CMClientStatusSetting.md)

[Update-CMClientStatus](Update-CMClientStatus.md)


