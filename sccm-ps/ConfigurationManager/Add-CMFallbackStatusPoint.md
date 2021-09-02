---
description: Add a fallback status point to a Configuration Manager site.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/23/2021
schema: 2.0.0
title: Add-CMFallbackStatusPoint
---

# Add-CMFallbackStatusPoint

## SYNOPSIS

Add a fallback status point to a Configuration Manager site.

## SYNTAX

### ByValue (Default)
```
Add-CMFallbackStatusPoint -InputObject <IResultObject> [-StateMessageCount <Int32>] [-ThrottleMins <Int32>]
 [-ThrottleSec <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Add-CMFallbackStatusPoint [-SiteCode <String>] [-SiteSystemServerName] <String> [-StateMessageCount <Int32>]
 [-ThrottleMins <Int32>] [-ThrottleSec <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add a fallback status point to a Configuration Manager site. The fallback status point is a site system role that helps you monitor client installation. It identifies clients that are unmanaged because they can't communicate with their management point. Although this role is supported only at primary sites, you can install multiple instances of this role at a site, and at multiple sites in the same hierarchy. For more information, see [Determine the site system roles for Configuration Manager clients](/mem/configmgr/core/clients/deploy/plan/determine-the-site-system-roles-for-clients#fallback-status-point).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a fallback status point

This command adds a fallback status point for site **CM1**. The command also specifies number of messages and throttle time period for the fallback status point.

```powershell
Add-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "CMFSPPoint.Western.Contoso.com" -StateMessageNum 10000 -ThrottleInterval 60
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

### -InputObject

Specify a site system server object as the target for this role. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode

Specify the site code for this site system role.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName

Specify the FQDN of the server as the target for this role.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StateMessageCount

Specify the number of state messages that Configuration Manager can process within the throttle interval. Use either **ThrottleMins** or **ThrottleSec** to configure the throttle interval.

When the site server processes many state messages, it might decrease the performance of the site server. For more information, see [Configuration options for site system roles - Fallback status point](/mem/configmgr/core/servers/deploy/configure/configuration-options-for-site-system-roles#BKMK_Fallback_Status_Point).

By default, this value is `10000`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StateMessagesCount, StateMessageNum

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleMins

Configure the throttle interval in minutes for how Configuration Manager processes the state messages. Use this parameter with **StateMessageCount**.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleSec

Configure the throttle interval in seconds for how Configuration Manager processes the state messages. Use this parameter with **StateMessageCount**.

By default, this value is `3600`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ThrottleIntervalSeconds, ThrottleInterval

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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_SCI_SysResUse
## NOTES

For more information on this return object and its properties, see [SMS_SCI_SysResUse server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_sysresuse-server-wmi-class).

## RELATED LINKS

[Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md)

[Remove-CMFallbackStatusPoint](Remove-CMFallbackStatusPoint.md)

[Set-CMFallbackStatusPoint](Set-CMFallbackStatusPoint.md)

[Determine the site system roles for Configuration Manager clients](/mem/configmgr/core/clients/deploy/plan/determine-the-site-system-roles-for-clients#fallback-status-point)
