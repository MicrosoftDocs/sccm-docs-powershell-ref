---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/15/2021
schema: 2.0.0
title: Set-CMSoftwareUpdatePoint
---

# Set-CMSoftwareUpdatePoint

## SYNOPSIS

Configure a software update point.

## SYNTAX

### ByValue (Default)
```
Set-CMSoftwareUpdatePoint [-AnonymousWsusAccess] [-ClientConnectionType <ClientConnectionTypes>]
 [-EnableCloudGateway <Boolean>] [-EnableSsl <Boolean>] [-HttpPort <Int32>] [-HttpsPort <Int32>]
 -InputObject <IResultObject> [-NlbVirtualIP <String>] [-PassThru] [-PublicVirtualIP <String>]
 [-UseProxy <Boolean>] [-UseProxyForAutoDeploymentRule <Boolean>] [-WsusAccessAccount <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMSoftwareUpdatePoint [-AnonymousWsusAccess] [-ClientConnectionType <ClientConnectionTypes>]
 [-EnableCloudGateway <Boolean>] [-EnableSsl <Boolean>] [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-NlbVirtualIP <String>] [-PassThru] [-PublicVirtualIP <String>] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-UseProxy <Boolean>] [-UseProxyForAutoDeploymentRule <Boolean>]
 [-WsusAccessAccount <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to change settings for a software update point site system role.

Configure the settings that a software update point uses when connecting with clients and with a WSUS server. To configure the site component for software update point, use the [Set-CMSoftwareUpdatePointComponent](Set-CMSoftwareUpdatePointComponent.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify the ports

This command modifies the ports for the site system server for the site code CM1.

```powershell
Set-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "CMSoftwareUpdatePoint.TSQA.Contoso.com" -HttpPort 8530 -HttpsPort 8531
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
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSsl

Set this parameter to `$true` to require SSL communication to the WSUS server.

For more information, see [Configure a software update point to use TLS/SSL with a PKI certificate](/mem/configmgr/sum/get-started/software-update-point-ssl).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: SslWsus, WsusSsl

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

### -HttpPort

Specify an integer value for the HTTP port to use for the WSUS server. By default, this value is `8530`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: WsusIisPort

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpsPort

Specify an integer value for the HTTPS port to use for the WSUS server. By default, this value is `8531`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: WsusIisSslPort

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a site system server object on which to configure the software update point role. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SoftwareUpdatePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NlbVirtualIP

Failover support for a software update point in a network load balancing (NLB) cluster was deprecated in version 1702. For more information, see [Removed and deprecated features](/mem/configmgr/core/plan-design/changes/deprecated/removed-and-deprecated-cmfeatures#unsupported-and-removed-features).

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

### -PublicVirtualIP

Specify a public virtual IP address for a software update point that's connected to the internet.

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

Specify the three-character code for the site that manages the system role for the software update point.

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

Specify the name of the site system server that hosts the software update point role.

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

### -WsusAccessAccount

Specify the user name for the WSUS server connection account. This account provides authenticated access from the site to the WSUS server. For more information, see [Accounts used in Configuration Manager](/mem/configmgr/core/plan-design/hierarchy/accounts#software-update-point-connection-account).

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

[Add-CMSoftwareUpdatePoint](Add-CMSoftwareUpdatePoint.md)

[Get-CMSoftwareUpdatePoint](Get-CMSoftwareUpdatePoint.md)

[Remove-CMSoftwareUpdatePoint](Remove-CMSoftwareUpdatePoint.md)

[Set-CMSoftwareUpdatePointComponent](Set-CMSoftwareUpdatePointComponent.md)
