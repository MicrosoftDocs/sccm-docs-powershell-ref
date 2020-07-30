---
description: Adds an Application Catalog web service point to a Configuration Manager site.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/27/2019
schema: 2.0.0
title: Add-CMApplicationCatalogWebServicePoint
---

# Add-CMApplicationCatalogWebServicePoint

## SYNOPSIS
Adds an Application Catalog web service point to Configuration Manager.

## SYNTAX

### WebServicePointByValue (Default)
```
Add-CMApplicationCatalogWebServicePoint [-WebsiteName <String>] [-WebApplicationName <String>]
 [-PortNumber <Int32>] [-CommunicationType <ComputerCommunicationType>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### WebServicePointByName
```
Add-CMApplicationCatalogWebServicePoint [-WebsiteName <String>] [-WebApplicationName <String>]
 [-PortNumber <Int32>] [-SiteSystemServerName] <String> [-SiteCode <String>]
 [-CommunicationType <ComputerCommunicationType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMApplicationCatalogWebServicePoint** cmdlet adds an Application Catalog web service point to a Configuration Manager site.

Configuration Manager requires a web service point site system role to support the Application Catalog website and the Software Library.
You also need an Application Catalog website point in the same site, but not necessarily on the same server.
If you intend to use Secure Hypertext Transfer Protocol (HTTPS), you need to deploy a web server certificate on the server hosting the web service point.
For more information about site system roles, see [Install and Configure Site System Roles for Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh272770(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a web service point for the Application Catalog
```
PS XYZ:\>Add-CMApplicationCatalogWebServicePoint -PortNumber 80 -SiteCode "CM1" -SiteSystemServerName "CMACWSPRole.Western.Contoso.com"
```

This command adds a web service point for the Application Catalog.
The command specifies a port for the service.
The command specifies the site code for the site that the role belongs to, as well as the name of the server that hosts the role.

## PARAMETERS

### -CommunicationType
Specifies the communication type.
Valid values are: HTTP and HTTPS.

```yaml
Type: ComputerCommunicationType
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

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

### -ForceWildcardHandling
Indicates that the cmdlet forces wild card handling.

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
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: WebServicePointByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PortNumber
Specifies the port to use to connect with the web service.

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

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: WebServicePointByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server that hosts a site system role.

```yaml
Type: String
Parameter Sets: WebServicePointByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplicationName
Specifies the name of the web application used for the application catalog.

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

### -WebsiteName
```yaml
Type: String
Parameter Sets: (All)
Aliases: IISWebSite

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Add-CMApplicationCatalogWebsitePoint](Add-CMApplicationCatalogWebsitePoint.md)

[Get-CMApplicationCatalogWebServicePoint](Get-CMApplicationCatalogWebServicePoint.md)

[Get-CMApplicationCatalogWebsitePoint](Get-CMApplicationCatalogWebsitePoint.md)

[Remove-CMApplicationCatalogWebServicePoint](Remove-CMApplicationCatalogWebServicePoint.md)


