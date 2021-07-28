---
description: Get the site system server role.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2020
schema: 2.0.0
title: Get-CMSiteSystemServer
---

# Get-CMSiteSystemServer

## SYNOPSIS

Get the site system server role.

## SYNTAX

### SearchByName (Default)
```
Get-CMSiteSystemServer [-AllSite] [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMSiteSystemServer [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the site system server role. A server with the **Site system** role hosts one or more other roles for a Configuration Manager site.

To get specific site system roles, use one of the following cmdlets:

- [Get-CMAssetIntelligenceSynchronizationPoint](Get-CMAssetIntelligenceSynchronizationPoint.md)
- [Get-CMCertificateRegistrationPoint](Get-CMCertificateRegistrationPoint.md)
- [Get-CMCloudManagementGatewayConnectionPoint](Get-CMCloudManagementGatewayConnectionPoint.md)
- [Get-CMDataWarehouseServicePoint](Get-CMDataWarehouseServicePoint.md)
- [Get-CMDistributionPoint](Get-CMDistributionPoint.md)
- [Get-CMEndpointProtectionPoint](Get-CMEndpointProtectionPoint.md)
- [Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md)
- [Get-CMManagementPoint](Get-CMManagementPoint.md)
- [Get-CMMulticastServicePoint](Get-CMMulticastServicePoint.md)
- [Get-CMReportingServicePoint](Get-CMReportingServicePoint.md)
- [Get-CMServiceConnectionPoint](Get-CMServiceConnectionPoint.md)
- [Get-CMSoftwareUpdatePoint](Get-CMSoftwareUpdatePoint.md)
- [Get-CMStateMigrationPoint](Get-CMStateMigrationPoint.md)

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a site system server

This command gets the site system server named **Server2.contoso.com** for site code **MP5**.

```powershell
Get-CMSiteSystemServer -SiteSystemServerName "Server2.contoso.com" -SiteCode "MP5"
```

## PARAMETERS

### -AllSite

Add this parameter to look for the site system server across all sites.

To specify a specific site, use the **SiteCode** parameter.

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

Specify a site system object **SMS_SCI_SysResUse** with role name `SMS Site System`.

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

Specify a Configuration Manager site code to look for the site system server.

To look across all sites, use the **AllSite** parameter.

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

Specify a server name for the site system to get.

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

## RELATED LINKS

[New-CMSiteSystemServer](New-CMSiteSystemServer.md)

[Remove-CMSiteSystemServer](Remove-CMSiteSystemServer.md)

[Set-CMSiteSystemServer](Set-CMSiteSystemServer.md)
