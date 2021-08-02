---
description: Get a site role object.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/25/2020
schema: 2.0.0
title: Get-CMSiteRole
---

# Get-CMSiteRole

## SYNOPSIS

Get a site role object.

## SYNTAX

### SearchByName (Default)
```
Get-CMSiteRole [-AllSite] [-RoleName <String>] [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMSiteRole [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Returns the roles installed on a Configuration Manager site system server. For example, a management point or distribution point.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all roles from all sites

This example gets all roles for all sites in the hierarchy.

```powershell
Get-CMSiteRole -AllSite
```

### Example 2: Get all roles for a specific site

This example gets all roles from the site **P01**.

```powershell
Get-CMSiteRole -SiteCode P01
```

### Example 3: Get roles for a specific server

This example gets all roles installed on the site system **cm01.contoso.local**.

```powershell
Get-CMSiteRole -SiteSystemServerName "cm01.contoso.local"
```

### Example 4: Count all management points

This example gets all of the management points in the hierarchy, and displays the count.

```powershell
$mp = Get-CMSiteRole -RoleName "SMS Management Point" -AllSite
$mp.Count
```

### Example 5: List all roles by name

This example lists the role names for all sites in the hierarchy.

```powershell
$allRoles = Get-CMSiteRole -AllSite
$allRoles.RoleName
```

## PARAMETERS

### -AllSite

Include this parameter to get all of the roles for the site.

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

### -RoleName

Specify a specific role name to get. The value is the string from the **RoleName** property on the **SMS_SCI_SysResUse** class. For example:

- `SMS Site System`
- `SMS Component Server`
- `SMS Distribution Point`
- `SMS Management Point`
- `SMS Device Management Point`
- `SMS Software Update Point`
- `SMS Enrollment Server`
- `SMS Enrollment Web Site`
- `SMS Notification Server`
- `SMS Certificate Registration Point`
- `SMS DM Enrollment Service`
- `SMS Site Server`
- `SMS State Migration Point`
- `SMS Provider`
- `SMS Cloud Proxy Connector`
- `SMS SQL Server`
- `SMS Fallback Status Point`
- `AI Update Service Point`
- `SMS SRS Reporting Point`
- `SMS Endpoint Protection Point`
- `Data Warehouse Service Point`
- `SMS Dmp Connector`

> [!NOTE]
> This list may not include all possible site roles.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -SiteCode

Specify the site code for the specific site role.

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

Specify the name of a specific site system server from which to get the role.

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

[Remove-CMSiteRole](Remove-CMSiteRole.md)

[Get-CMSiteFeature](Get-CMSiteFeature.md)

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)
