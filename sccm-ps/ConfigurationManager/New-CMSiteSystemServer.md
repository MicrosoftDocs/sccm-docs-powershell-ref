---
description: Creates a site system server.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMSiteSystemServer
---

# New-CMSiteSystemServer

## SYNOPSIS
Creates a site system server.

## SYNTAX

```
New-CMSiteSystemServer [-SiteCode <String>] [-SiteSystemServerName] <String> [-PublicFqdn <String>]
 [-FdmOperation <Boolean>] [-UseSiteServerAccount] [-AccountName <String>] [-EnableProxy <Boolean>]
 [-ProxyServerName <String>] [-ProxyServerPort <UInt32>] [-ProxyAccessAccount <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSiteSystemServer** cmdlet creates a site system server in Microsoft System Center Configuration Manager.
A site system server provides functionality to a configuration management site, such as communication between a Configuration Manager server and Configuration Manager clients.
You can designate a new server as a site system server and add the site system roles, or install site system roles to an existing site system server in the site.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a site system server
```
PS XYZ:\> New-CMSiteSystemServer -SiteSystemServerName "Server1.contoso.com" -SiteCode "MP5" -PublicFqdn "Internetsrv1.contoso.com" -FdmOperation $True -UseSiteServerAccount -EnableProxy $True -ProxyServerName "ProxyServer1" -ProxyServerPort 80 -ProxyAccessAccount (Get-CMAccount "contoso\administrator")
```

This command creates a site system server with the name Server1.contoso.com.
The site system server uses the proxy server named ProxyServer1 to connect to the Internet using port 80.

## PARAMETERS

### -AccountName
Specifies an account name to use to install the site system server.

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

### -EnableProxy
Indicates whether to enable a proxy server to use when synchronizing information from the Internet.

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
Indicates whether the site server is required to initiate connections to this site system.

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

### -ProxyAccessAccount
Specifies the credentials to use to authenticate with the proxy server.
Do not use user principal name (UPN) format.

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
Specifies the name of a proxy server.
Use a fully qualified domain name (FQDN), short name, or IPv4/IPv6 address.

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
Specifies the proxy server port number to use when connecting to the Internet.

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
Specifies a fully qualified domain name (FQDN) for the site system for use on the Internet.

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
Specifies the site code for a Configuration Manager site.

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
Specifies a name for the site system server.

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
Indicates that the cmdlet uses the computer account of the site server to install the site system.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Get-CMAccount](Get-CMAccount.md)

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[Remove-CMSiteSystemServer](Remove-CMSiteSystemServer.md)

[Set-CMSiteSystemServer](Set-CMSiteSystemServer.md)


