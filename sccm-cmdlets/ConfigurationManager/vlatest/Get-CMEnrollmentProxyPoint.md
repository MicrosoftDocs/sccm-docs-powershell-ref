---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833694
schema: 2.0.0
ms.assetid: 7DDE98A2-66EF-4751-95B6-13684209508F
---

# Get-CMEnrollmentProxyPoint

## SYNOPSIS
Gets an enrollment proxy point.

## SYNTAX

### SearchByName
```
Get-CMEnrollmentProxyPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMEnrollmentProxyPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEnrollmentProxyPoint** cmdlet gets a Microsoft System Center Configuration Manager enrollment proxy point.
An enrollment proxy point is a site system role that manages enrollment requests from mobile devices.

## EXAMPLES

### Example 1: Get an enrollment proxy point
```
PS C:\> Get-CMEnrollmentProxyPoint -SiteCode "CM1" -SiteSystemServerName "SiteServer01.Contoso.com"
```

This command gets an enrollment proxy point.

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
Specifies a site code.

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
Specifies the fully qualified domain name (FQDN) of the server that hosts the site system role.

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

[Add-CMEnrollmentProxyPoint](./Add-CMEnrollmentProxyPoint.md)

[Remove-CMEnrollmentProxyPoint](./Remove-CMEnrollmentProxyPoint.md)


