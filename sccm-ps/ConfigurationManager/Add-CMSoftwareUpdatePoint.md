---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/15/2021
schema: 2.0.0
title: Add-CMSoftwareUpdatePoint
---

# Add-CMSoftwareUpdatePoint

## SYNOPSIS

Add a software update point.

## SYNTAX

### SumPByValueWithWsus (Default)
```
Add-CMSoftwareUpdatePoint [-AnonymousWsusAccess] [-ClientConnectionType <ClientConnectionTypes>]
 [-ConnectionAccountUserName <String>] [-EnableCloudGateway] -InputObject <IResultObject> [-UseProxy <Boolean>]
 [-UseProxyForAutoDeploymentRule <Boolean>] [-WsusIisPort <Int32>] [-WsusIisSslPort <Int32>]
 [-WsusSsl <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SumPWithWsus
```
Add-CMSoftwareUpdatePoint [-AnonymousWsusAccess] [-ClientConnectionType <ClientConnectionTypes>]
 [-ConnectionAccountUserName <String>] [-EnableCloudGateway] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-UseProxy <Boolean>] [-UseProxyForAutoDeploymentRule <Boolean>]
 [-WsusIisPort <Int32>] [-WsusIisSslPort <Int32>] [-WsusSsl <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add a software update point to the site. This site system role hosts the Windows Software Update Services (WSUS) processes.

After you add the role, use the [Set-CMSoftwareUpdatePointComponent](Set-CMSoftwareUpdatePointComponent.md) cmdlet to configure the site component.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a software update point

This command adds a software update point on the computer named CMSoftwareUpdatePoint.TSQA.Contoso.com for the Configuration Manager site that has the site code CM1.

```powershell
Add-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "CMSoftwareUpdatePoint.TSQA.Contoso.com"
```

## PARAMETERS

### -AnonymousWsusAccess

Add this parameter to indicates that the software update point allows anonymous WSUS access.

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

### -ClientConnectionType

Specify the type of the client connection.

```yaml
Type: ClientConnectionTypes
Parameter Sets: (All)
Aliases:
Accepted values: Intranet, Internet, InternetAndIntranet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionAccountUserName

Specify the user name for the WSUS server connection account. This account provides authenticated access from the site to the WSUS server. For more information, see [Accounts used in Configuration Manager](/mem/configmgr/core/plan-design/hierarchy/accounts#software-update-point-connection-account).

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserName

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

### -EnableCloudGateway

Add this parameter to allow cloud management gateway (CMG) traffic to this software update point.

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

Specify a site system server object on which to add the software update point role. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SumPByValueWithWsus
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
Parameter Sets: SumPWithWsus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName

Specify the name of the site system server to host the software update point role.

```yaml
Type: String
Parameter Sets: SumPWithWsus
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseProxy

Set this parameter to `$true` to use a proxy server for software updates.

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

### -UseProxyForAutoDeploymentRule

When you use the **UseProxy** parameter, set this parameter to `$true` to use a proxy server when downloading content with an automatic deployment rule (ADR).

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

### -WsusIisPort

Specify an integer value for the HTTP port to use for the WSUS server. By default, this value is `8530`.

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

### -WsusIisSslPort

Specify an integer value for the HTTPS port to use for the WSUS server. By default, this value is `8531`.

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

### -WsusSsl

Set this parameter to `$true` to require SSL communication to the WSUS server.

For more information, see [Configure a software update point to use TLS/SSL with a PKI certificate](/mem/configmgr/sum/get-started/software-update-point-ssl).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: SslWsus

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

[Get-CMSoftwareUpdatePoint](Get-CMSoftwareUpdatePoint.md)

[Remove-CMSoftwareUpdatePoint](Remove-CMSoftwareUpdatePoint.md)

[Set-CMSoftwareUpdatePoint](Set-CMSoftwareUpdatePoint.md)

[Set-CMSoftwareUpdatePointComponent](Set-CMSoftwareUpdatePointComponent.md)
