---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/15/2021
schema: 2.0.0
title: Get-CMSoftwareUpdatePointComponent
---

# Get-CMSoftwareUpdatePointComponent

## SYNOPSIS

Get the site component for the software update point.

## SYNTAX

```
Get-CMSoftwareUpdatePointComponent [-SiteCode <String>] [-SiteSystemServerName <String>] [-WsusSyncManager]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the site component for the software update point. You can use the cmdlet to view the component configuration, or to get an object to configure with the [Set-CMSoftwareUpdatePointComponent](Set-CMSoftwareUpdatePointComponent.md) cmdlet.

A software update point component interacts with a Windows Server Update Services (WSUS) server to configure update settings, request synchronization to the upstream update source, and synchronize updates from the WSUS database to the site server database on the central site.

For more information, see [Site components for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-components).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a software update point component by name

This command gets a software update point component by using the site system server name.

```powershell
Get-CMSoftwareUpdatePointComponent -SiteSystemServerName "Contoso-SiteSysSrv.Western.Contoso.com"
```

### Example 2: Get a software update point component by site code

This command gets a software update point component by using the site code.

```powershell
Get-CMSoftwareUpdatePointComponent -SiteCode "CM1"
```

### Example 3: Show the status of third-party updates in the hierarchy

```powershell
$SUPWsusSyncMgr = Get-CMSoftwareUpdatePointComponent -WsusSyncManager

$SUPWsusSyncMgr.Props | Where PropertyName -eq "EnableThirdPartyUpdates"
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

### -SiteCode

Specify the three-character code for the site from which to get the software update point component.

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

Specify the FQDN of a site system server that has the software update point role.

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

### -WsusSyncManager

By default, this cmdlet gets objects and properties from the **SMS_WSUS_CONFIGURATION_MANAGER** component. Add this parameter to get objects and properties from the **SMS_WSUS_SYNC_MANAGER** component.

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

### IResultObject[]#SMS_SCI_Component

### IResultObject#SMS_SCI_Component

## NOTES

For more information on this return object and its properties, see [SMS_SCI_Component server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_component-server-wmi-class).

## RELATED LINKS

[Set-CMSoftwareUpdatePointComponent](Set-CMSoftwareUpdatePointComponent.md)

[Site components for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-components)
