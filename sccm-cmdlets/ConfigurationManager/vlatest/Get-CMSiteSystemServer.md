---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833881
schema: 2.0.0
ms.assetid: 099289E2-E483-4312-B9E4-0CA86E6CE904
---

# Get-CMSiteSystemServer

## SYNOPSIS
Gets a site system server.

## SYNTAX

### SearchByName
```
Get-CMSiteSystemServer [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMSiteSystemServer -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSiteSystemServer** cmdlet gets a site system server in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get a site system server
```
PS C:\>Get-CMSiteSystemServer -SiteSystemServerName "Server2.contoso.com" -SiteCode "MP5"
```

This command gets the site system server named Server2.contoso.com for site code MP5.

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
Specifies a site system object.

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
Specifies a site code for a Configuration Manager site.

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
Specifies a server name for the site system.

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

### IResultObject[]#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[New-CMSiteSystemServer](./New-CMSiteSystemServer.md)

[Remove-CMSiteSystemServer](./Remove-CMSiteSystemServer.md)

[Set-CMSiteSystemServer](./Set-CMSiteSystemServer.md)


