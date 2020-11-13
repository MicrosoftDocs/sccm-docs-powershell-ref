---
description: Creates a new Windows Firewall policy in Configuration Manager.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMWindowsFirewallPolicy
---

# New-CMWindowsFirewallPolicy

## SYNOPSIS
Creates a new Windows Firewall policy in Configuration Manager.

## SYNTAX

```
New-CMWindowsFirewallPolicy [-Description <String>] [-DomainBlockAllInboundTraffic <SettingType>]
 [-DomainNotification <SettingType>] [-DomainTurnOnFirewall <SettingType>] -Name <String>
 [-PrivateBlockAllInboundTraffic <SettingType>] [-PrivateNotification <SettingType>]
 [-PrivateTurnOnFirewall <SettingType>] [-PublicBlockAllInboundTraffic <SettingType>]
 [-PublicNotification <SettingType>] [-PublicTurnOnFirewall <SettingType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMWindowsFirewallPolicy** cmdlet creates a configuration policy for Windows Firewall in Configuration Manager.

Windows Firewall allows or denies incoming connections to an IP address.
The blocking actions allow or deny incoming traffic based on a network location type.
The network location types are: domain, public, and private.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a Windows Firewall policy
```
PS XYZ:\> New-CMWindowsFirewallPolicy -Name "test01" -Description "323132" -DomainTurnOnFirewall Yes -PrivateTurnOnFirewall Yes -PublicTurnOnFirewall Yes
```

This command creates a new Windows Firewall policy and enables the firewall for domain, private, and public network location types.

## PARAMETERS

### -Description
Specifies a description for the firewall policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

Required: False
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

### -DomainBlockAllInboundTraffic
Specifies whether to block all incoming traffic for a domain type of network location.The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNotification
```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: DomainNotifications
Accepted values: Yes, No, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainTurnOnFirewall
Specifies whether to turn on a firewall for a domain type of network location.
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured

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

### -Name
Specifies a name for the firewall policy in Configuration Manager.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateBlockAllInboundTraffic
Specifies whether to block all incoming traffic for a private type of network location.
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateNotification
```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: PrivateNotifications
Accepted values: Yes, No, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateTurnOnFirewall
Specifies whether to turn on a firewall for a private type of network location.
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicBlockAllInboundTraffic
Specifies whether to block all incoming traffic for a public type of network location.
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNotification
```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: PublicNotifications
Accepted values: Yes, No, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicTurnOnFirewall
Specifies whether to enable Windows Firewall for a public network location.
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Set-CMWindowsFirewallPolicy](Set-CMWindowsFirewallPolicy.md)


