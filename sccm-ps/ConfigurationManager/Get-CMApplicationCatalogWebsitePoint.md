---
description: Gets a Configuration Manager Application Catalog website point.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Get-CMApplicationCatalogWebsitePoint
---

# Get-CMApplicationCatalogWebsitePoint

## SYNOPSIS
Gets a Configuration Manager Application Catalog website point.

## SYNTAX

### SearchByName (Default)
```
Get-CMApplicationCatalogWebsitePoint [-AllSite] [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMApplicationCatalogWebsitePoint [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMApplicationCatalogWebsitePoint** cmdlet gets an Application Catalog website point in Configuration Manager.
This site system role supports the Application Catalog website.

You can specify a website point by either site code or by the name of the server that hosts the role.
Use this cmdlet with no parameters to get all Application Catalog website points for a Configuration Manager hierarchy.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a website point by using a site code
```
PS XYZ:\> Get-CMApplicationCatalogWebsitePoint -SiteCode "CM4"
```

This command gets the website point role for the site that has the site code CM4.

### Example 2: Get a website point by using a site system name
```
PS XYZ:\> Get-CMApplicationCatalogWebsitePoint -SiteSystemServerName "WesternACWP.Contoso.com"
```

This command gets the website point role that the computer WesternACWP.Contoso.com hosts.

## PARAMETERS

### -AllSite
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

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

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
Specifies the site code for a Configuration Manager site.

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
Specifies the name of a server that hosts a site system role.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

[Add-CMApplicationCatalogWebServicePoint](Add-CMApplicationCatalogWebServicePoint.md)

[Add-CMApplicationCatalogWebsitePoint](Add-CMApplicationCatalogWebsitePoint.md)

[Get-CMApplicationCatalogWebServicePoint](Get-CMApplicationCatalogWebServicePoint.md)

[Remove-CMApplicationCatalogWebSitePoint](Remove-CMApplicationCatalogWebSitePoint.md)

[Set-CMApplicationCatalogWebsitePoint](Set-CMApplicationCatalogWebsitePoint.md)


