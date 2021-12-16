---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/15/2021
schema: 2.0.0
title: Get-CMSoftwareUpdatePoint
---

# Get-CMSoftwareUpdatePoint

## SYNOPSIS

Get a software update point.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdatePoint [-AllSite] [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMSoftwareUpdatePoint [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a software update point site system role.

A software update point is a site server role that hosts software updates.
Configuration Manager clients connect to a software update point to get available updates.
The software update point interacts with Windows Server Update Services (WSUS) to configure update settings, request synchronization to the update source, and to synchronize software updates from the WSUS database.

For more information, see [Plan for software updates in Configuration Manager](/mem/configmgr/sum/plan-design/plan-for-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a software update point

The command gets a software update point that UpdateSystem.Western.Contoso.com hosts.

```powershell
Get-CMSoftwareUpdatePoint -SiteSystemServerName "UpdateSystem.Western.Contoso.com"
```

## PARAMETERS

### -AllSite

Add this parameter to get the software update points from all sites in the hierarchy.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AllSites

Required: False
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

### -InputObject

Specify a site system server object that has the software update point role. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode

Specify the three-character code for the site that manages the system role for the software update point.

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

### -SiteSystemServerName

Specify the name of the site system server that hosts the software update point role.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_SCI_SysResUse

### IResultObject#SMS_SCI_SysResUse

## NOTES

For more information on this return object and its properties, see [SMS_SCI_SysResUse server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_sysresuse-server-wmi-class).

## RELATED LINKS

[Add-CMSoftwareUpdatePoint](Add-CMSoftwareUpdatePoint.md)

[Remove-CMSoftwareUpdatePoint](Remove-CMSoftwareUpdatePoint.md)

[Set-CMSoftwareUpdatePoint](Set-CMSoftwareUpdatePoint.md)
