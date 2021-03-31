---
description: Changes settings for a Configuration Manager software update point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSoftwareUpdatePoint
---

# Set-CMSoftwareUpdatePoint

## SYNOPSIS
Changes settings for a Configuration Manager software update point.

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
The **Set-CMSoftwareUpdatePoint** cmdlet changes settings for a software update point in Configuration Manager.

A software update point is a site server role that hosts software updates.
Configuration Manager clients connect to a software update point to get available updates.
The software update point interacts with Windows Server Update Services (WSUS) to configure update settings, request synchronization to the update source, and to synchronize software updates from the WSUS database.

You can use this cmdlet to configure the settings a software update point uses when connecting with clients and with a WSUS server.
These settings include Network Load Balancing (NLB), a virtual IP address, Internet Information Services (IIS) port, and whether to use Secure Socket Locket Layer (SSL) to connect with WSUS.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify the server name
```
PS XYZ:\> Set-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "CMSoftwareUpdatePoint.TSQA.Contoso.com"
```

This command modifies the name for the site system server for the site code CM1.

## PARAMETERS

### -AnonymousWsusAccess
Indicates that the software update point allows anonymous.

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
Specifies a connection type.
Clients can connect to the software update point in several ways.
You can configure the software update point to handle different types of connections differently by specifying the connection type.
Valid values are:

- Internet
- InternetAndIntranet
- Intranet

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
Indicates that the cmdlet enables SSL for the update point.

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
Specifies a software update point object.
To obtain a software update point object, use the [Get-CMSoftwareUpdatePoint](Get-CMSoftwareUpdatePoint.md) cmdlet.

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
Specifies an IP address or host name.
If this software update point uses load balancing, this is the NLB address.

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
Specifies a public virtual IP address for a software update point that is connected to over the Internet.

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
Specifies a site code for a Configuration Manager site.

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
Specifies the name of the computer that hosts the software update point site system role.

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
Specifies whether a software update point can use a proxy.

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
Indicates whether an auto deployment rule can use a proxy.

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
Specifies an access account.
Unless a software update point allows anonymous access, use this access account to connect to it.

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

## RELATED LINKS

[Add-CMSoftwareUpdatePoint](Add-CMSoftwareUpdatePoint.md)

[Get-CMSoftwareUpdatePoint](Get-CMSoftwareUpdatePoint.md)

[Remove-CMSoftwareUpdatePoint](Remove-CMSoftwareUpdatePoint.md)
