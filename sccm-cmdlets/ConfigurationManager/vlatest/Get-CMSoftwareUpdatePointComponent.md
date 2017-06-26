---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 5AAD5A9E-3547-47A3-8CB3-0E0DC066AACE
online version: https://go.microsoft.com/fwlink/?linkid=833925
schema: 2.0.0
---

# Get-CMSoftwareUpdatePointComponent

## SYNOPSIS
Retrieves a software update point component in Configuration Manager.

## SYNTAX

```
Get-CMSoftwareUpdatePointComponent [-SiteSystemServerName <String>] [-SiteCode <String>] [-WsusSyncManager]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdatePointComponent** cmdlet retrieves a software update point component.
A software update point component interacts with WSUS services to configure update settings, request synchronization to the upstream update source, and synchronize updates from the WSUS database to the site server database on the central site.

## EXAMPLES

### Example 1: Retrieve a software update point component by name
```
PS C:\> Get-CMSoftwareUpdatePointComponent -SiteSystemServerName "Contoso-SiteSysSrv.Western.Contoso.com"
```

This command retrieves a software update point component by using the site system server name.

### Example 2: Retrieve a software update point component by site code
```
PS C:\> Get-CMSoftwareUpdatePointComponent -SiteCode "CM1"
```

This command retrieves a software update point component by using the site code.

## PARAMETERS

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

### -SiteCode
Specifies a site code in Configuration Manager.

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
Specifies an array of names of a site system servers in Configuration Manager.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WsusSyncManager
{{Fill WsusSyncManager Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSoftwareUpdatePointComponent](./Set-CMSoftwareUpdatePointComponent.md)


