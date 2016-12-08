---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834091
schema: 2.0.0
ms.assetid: 4381D90C-738B-4526-A0FF-7B1A36851F41
---

# Get-CMApplicationCatalogWebsitePoint

## SYNOPSIS
Gets a Configuration Manager Application Catalog website point.

## SYNTAX

### SearchByName
```
Get-CMApplicationCatalogWebsitePoint [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMApplicationCatalogWebsitePoint -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMApplicationCatalogWebsitePoint** cmdlet gets an Application Catalog website point in Microsoft System Center Configuration Manager.
This site system role supports the Application Catalog website.

You can specify a website point by either site code or by the name of the server that hosts the role.
Use this cmdlet with no parameters to get all Application Catalog website points for a Configuration Manager hierarchy.

## EXAMPLES

### Example 1: Get a website point by using a site code
```
PS C:\> Get-CMApplicationCatalogWebsitePoint -SiteCode "CM4"
```

This command gets the website point role for the site that has the site code CM4.

### Example 2: Get a website point by using a site system name
```
PS C:\> Get-CMApplicationCatalogWebsitePoint -SiteSystemServerName "WesternACWP.Contoso.com"
```

This command gets the website point role that the computer WesternACWP.Contoso.com hosts.

## PARAMETERS

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMApplicationCatalogWebServicePoint](./Add-CMApplicationCatalogWebServicePoint.md)

[Add-CMApplicationCatalogWebsitePoint](./Add-CMApplicationCatalogWebsitePoint.md)

[Get-CMApplicationCatalogWebServicePoint](./Get-CMApplicationCatalogWebServicePoint.md)

[Remove-CMApplicationCatalogWebSitePoint](./Remove-CMApplicationCatalogWebSitePoint.md)

[Set-CMApplicationCatalogWebsitePoint](./Set-CMApplicationCatalogWebsitePoint.md)


