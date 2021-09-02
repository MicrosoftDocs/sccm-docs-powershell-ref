---
description: Configure the site system server role.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2020
schema: 2.0.0
title: Set-CMSiteSystemServer
---

# Set-CMSiteSystemServer

## SYNOPSIS

Configure the site system server role.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMSiteSystemServer [-AccountName <String>] [-EnableProxy <Boolean>] [-FdmOperation <Boolean>]
 -InputObject <IResultObject> [-PassThru] [-ProxyAccessAccount <IResultObject>] [-ProxyServerName <String>]
 [-ProxyServerPort <UInt32>] [-PublicFqdn <String>] [-UseSiteServerAccount] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMSiteSystemServer [-AccountName <String>] [-EnableProxy <Boolean>] [-FdmOperation <Boolean>] [-PassThru]
 [-ProxyAccessAccount <IResultObject>] [-ProxyServerName <String>] [-ProxyServerPort <UInt32>]
 [-PublicFqdn <String>] [-SiteCode <String>] [-SiteSystemServerName] <String> [-UseSiteServerAccount]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the site system server role. A server with the **Site system** role hosts one or more other roles for a Configuration Manager site.

To configure specific site system roles, use one of the following cmdlets:

- [Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md)
- [Set-CMCertificateRegistrationPoint](Set-CMCertificateRegistrationPoint.md)
- [Set-CMCloudManagementGatewayConnectionPoint](Set-CMCloudManagementGatewayConnectionPoint.md)
- [Set-CMDataWarehouseServicePoint](Set-CMDataWarehouseServicePoint.md)
- [Set-CMDistributionPoint](Set-CMDistributionPoint.md)
- [Set-CMEndpointProtectionPoint](Set-CMEndpointProtectionPoint.md)
- [Set-CMFallbackStatusPoint](Set-CMFallbackStatusPoint.md)
- [Set-CMManagementPoint](Set-CMManagementPoint.md)
- [Set-CMMulticastServicePoint](Set-CMMulticastServicePoint.md)
- [Set-CMReportingServicePoint](Set-CMReportingServicePoint.md)
- [Set-CMServiceConnectionPoint](Set-CMServiceConnectionPoint.md)
- [Set-CMSoftwareUpdatePoint](Set-CMSoftwareUpdatePoint.md)
- [Set-CMStateMigrationPoint](Set-CMStateMigrationPoint.md)

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a site system server

This command first uses the **Get-CMSiteSystemServer** cmdlet to get the site system server object for **Server2.contoso.com**. It then uses the pipeline operator to pass the object to **Set-CMSiteSystemServer**, which configures the server. It adds an FQDN to the server, and enables it to use a proxy server named **ProxyServer1** to connect to the internet using port 80.

```powershell
Get-CMSiteSystemServer -Name "Server2.contoso.com" -SiteCode "MP5" | Set-CMSiteSystemServer -PublicFqdn "Internetsrv2New.contoso.com" -FdmOperation $False -AccountName "contoso\cmsvc" -EnableProxy $True -ProxyServerName "ProxyServer1" -ProxyServerPort 80 -ProxyAccessAccount (Get-CMAccount "contoso\proxysvc") -PassThru
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

### -InputObject

Specify a site system server object to configure. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: SiteSystemServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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
Parameter Sets: SearchByNameMandatory
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
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[New-CMSiteSystemServer](New-CMSiteSystemServer.md)

[Remove-CMSiteSystemServer](Remove-CMSiteSystemServer.md)
