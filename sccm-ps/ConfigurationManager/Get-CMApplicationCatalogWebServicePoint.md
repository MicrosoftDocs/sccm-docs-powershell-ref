---
description: Gets an Application Catalog web service point.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Get-CMApplicationCatalogWebServicePoint
---

# Get-CMApplicationCatalogWebServicePoint

## SYNOPSIS
Gets an Application Catalog web service point.

## SYNTAX

### SearchByName (Default)
```
Get-CMApplicationCatalogWebServicePoint [-AllSite] [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMApplicationCatalogWebServicePoint [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMApplicationCatalogWebServicePoint** cmdlet gets a Configuration Manager Application Catalog web service point object that has a specified site code for a fully qualified domain name (FQDN).

Before you can configure an Application Catalog web service point you must first install and configure site system roles in Configuration Manager.
For more information, see [Install and Configure Site System Roles for Configuration Manager](https://docs.microsoft.com/mem/configmgr/core/servers/deploy/configure/install-site-system-roles).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a system role
```
PS XYZ:\> Get-CMApplicationCatalogWebServicePoint -SiteSystemServerName "western.contoso.com" -SiteCode "CM1"
```

This command gets an Application Catalog web service point named western.contoso.com that has the site code CM1.

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
Specifies a site code for an Application Catalog web service point object.

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
Specifies an FQDN for an Application Catalog web service point.

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

[Remove-CMApplicationCatalogWebServicePoint](Remove-CMApplicationCatalogWebServicePoint.md)


