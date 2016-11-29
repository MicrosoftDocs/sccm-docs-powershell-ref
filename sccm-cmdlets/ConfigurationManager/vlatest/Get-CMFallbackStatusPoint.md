---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833703
schema: 2.0.0
ms.assetid: F7D78486-A360-44AF-997A-37CDA8BB7844
---

# Get-CMFallbackStatusPoint

## SYNOPSIS
Gets a Configuration Manager fallback status point.

## SYNTAX

### SearchByName
```
Get-CMFallbackStatusPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMFallbackStatusPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMFallbackStatusPoint** cmdlet gets a fallback status point site server role.
You can get fallback status point for a site system name or a site code or both.

Microsoft System Center Configuration Manager can use one or more fallback status points to collect state messages for a site and send them on to Configuration Manager.
You can use this cmdlet to get a fallback status point to use with other cmdlets, such as the Set-CMFallbackStatusPoint cmdlet or the Remove-CMFallbackStatusPoint cmdlet.

## EXAMPLES

### Example 1: Get a fallback status point
```
PS C:\>Get-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "Server21.West01.Contoso.com"
```

This command gets a fallback status point for the site with the site code cm1 and the system name Server21.West01.Contoso.com.
You can have more than one fallback status point for a site.
This example specifies both the site code and the server name.

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
Specifies the site code for a fallback status point.

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
Specifies the site system name for a fallback status point.

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

[Add-CMFallbackStatusPoint](./Add-CMFallbackStatusPoint.md)

[Remove-CMFallbackStatusPoint](./Remove-CMFallbackStatusPoint.md)

[Set-CMFallbackStatusPoint](./Set-CMFallbackStatusPoint.md)


