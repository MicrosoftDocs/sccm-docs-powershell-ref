---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: F8EC64DE-F2D9-4AD0-86DB-0C978E8DD372
online version: https://go.microsoft.com/fwlink/?linkid=834087
schema: 2.0.0
---

# Get-CMApplicationCatalogWebServicePoint

## SYNOPSIS
Gets an Application Catalog web service point.

## SYNTAX

### SearchByName (Default)
```
Get-CMApplicationCatalogWebServicePoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-AllSite]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMApplicationCatalogWebServicePoint [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMApplicationCatalogWebServicePoint** cmdlet gets a Microsoft System Center Configuration Manager Application Catalog web service point object that has a specified site code for a fully qualified domain name (FQDN).

Before you can configure an Application Catalog web service point you must first install and configure site system roles in Configuration Manager.
For more information, see [Install and Configure Site System Roles for Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=262649) on TechNet.

## EXAMPLES

### Example 1: Get a system role
```
PS C:\> Get-CMApplicationCatalogWebServicePoint -SiteSystemServerName "western.contoso.com" -SiteCode "CM1"
```

This command gets an Application Catalog web service point named western.contoso.com that has the site code CM1.

## PARAMETERS

### -AllSite
{{Fill AllSite Description}}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMApplicationCatalogWebServicePoint](./Add-CMApplicationCatalogWebServicePoint.md)

[Remove-CMApplicationCatalogWebServicePoint](./Remove-CMApplicationCatalogWebServicePoint.md)


