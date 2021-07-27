---
description: Add a new site system server.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2020
schema: 2.0.0
title: New-CMSiteSystemServer
---

# New-CMSiteSystemServer

## SYNOPSIS

Add a new site system server.

## SYNTAX

```
New-CMSiteSystemServer [-AccountName <String>] [-EnableProxy <Boolean>] [-FdmOperation <Boolean>]
 [-ProxyAccessAccount <IResultObject>] [-ProxyServerName <String>] [-ProxyServerPort <UInt32>]
 [-PublicFqdn <String>] [-SiteCode <String>] [-SiteSystemServerName] <String> [-UseSiteServerAccount]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a new site system server. A server with the **Site system** role hosts one or more other roles for a Configuration Manager site.

To add specific site system roles, use one of the following cmdlets:

- [Add-CMAssetIntelligenceSynchronizationPoint](Add-CMAssetIntelligenceSynchronizationPoint.md)
- [Add-CMCertificateRegistrationPoint](Add-CMCertificateRegistrationPoint.md)
- [Add-CMCloudManagementGatewayConnectionPoint](Add-CMCloudManagementGatewayConnectionPoint.md)
- [Add-CMDataWarehouseServicePoint](Add-CMDataWarehouseServicePoint.md)
- [Add-CMDistributionPoint](Add-CMDistributionPoint.md)
- [Add-CMEndpointProtectionPoint](Add-CMEndpointProtectionPoint.md)
- [Add-CMFallbackStatusPoint](Add-CMFallbackStatusPoint.md)
- [Add-CMManagementPoint](Add-CMManagementPoint.md)
- [Add-CMMulticastServicePoint](Add-CMMulticastServicePoint.md)
- [Add-CMReportingServicePoint](Add-CMReportingServicePoint.md)
- [Add-CMServiceConnectionPoint](Add-CMServiceConnectionPoint.md)
- [Add-CMSoftwareUpdatePoint](Add-CMSoftwareUpdatePoint.md)
- [Add-CMStateMigrationPoint](Add-CMStateMigrationPoint.md)

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a site system server

```powershell
New-CMSiteSystemServer -SiteSystemServerName "Server1.contoso.com" -SiteCode "MP5" -PublicFqdn "Internetsrv1.contoso.com" -FdmOperation $True -UseSiteServerAccount -EnableProxy $True -ProxyServerName "ProxyServer1" -ProxyServerPort 80 -ProxyAccessAccount (Get-CMAccount "contoso\proxysvc")
```

## PARAMETERS

### -AccountName

Specify the account for installing this site system, and the account used for all connections from the site server. For more information, see [Site system installation account](/mem/configmgr/core/plan-design/hierarchy/accounts#site-system-installation-account).

To use the site server's computer account, use the **UseSiteServerAccount** parameter.

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

### -EnableProxy

Set this parameter to `$true` for the site system to use a proxy server when it synchronizes information from the internet.

If you enable this option, also configure the following parameters:

- ProxyServerName
- ProxyServerPort
- ProxyAccessAccount

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FdmOperation

Set this parameter to `$true` to require the site server to initiate connections to this site system.

```yaml
Type: Boolean
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

### -ProxyAccessAccount

If you set **EnableProxy** to `$true`, use this parameter to specify an account object. The site system uses these credentials to authenticate to the proxy server. To get this account object, use the [Get-CMAccount](Get-CMAccount.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProxyServerName

If you set **EnableProxy** to `$true`, use this parameter to specify the name of the proxy server. This parameter accepts the following types of values:

- Fully qualified domain name (FQDN)
- Hostname
- IPv4 or IPv6 address

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

### -ProxyServerPort

If you set **EnableProxy** to `$true`, use this parameter to specify the proxy server port number.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicFqdn

Specify an FQDN for the site system to use on the internet.

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

### -SiteCode

Specify the site code for this site system.

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

Specify the name of the site system server to configure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServerName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSiteServerAccount

Add this parameter to use the site server's computer account to install this site system. For more information, see [Site system installation account](/mem/configmgr/core/plan-design/hierarchy/accounts#site-system-installation-account).

To use another account, use the **UseSiteServerAccount** parameter.

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

### None
## OUTPUTS

### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[Remove-CMSiteSystemServer](Remove-CMSiteSystemServer.md)

[Set-CMSiteSystemServer](Set-CMSiteSystemServer.md)
