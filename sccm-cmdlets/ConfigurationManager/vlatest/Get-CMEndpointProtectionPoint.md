---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833681
schema: 2.0.0
ms.assetid: 6B74ECA1-5193-46F2-8C2F-976B6E5D6EAD
---

# Get-CMEndpointProtectionPoint

## SYNOPSIS
Gets an Endpoint Protection point.

## SYNTAX

### SearchByName
```
Get-CMEndpointProtectionPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMEndpointProtectionPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEndpointProtectionPoint** cmdlet gets a System Center 2016 Endpoint Protection point in Microsoft System Center Configuration Manager.
For more information about Endpoint Protection in Microsoft System Center Configuration Manager, see [Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427) on TechNet.

## EXAMPLES

### Example 1: Get an Endpoint Protection point
```
PS C:\>Get-CMEndpointProtectionPoint -SiteCode "CM1" -SiteSystemServerName "CMServer01.Contoso.com"
```

This command gets an Endpoint Protection point.

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

[Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427)

[Add-CMEndpointProtectionPoint](./Add-CMEndpointProtectionPoint.md)

[Remove-CMEndpointProtectionPoint](./Remove-CMEndpointProtectionPoint.md)

[Set-CMEndpointProtectionPoint](./Set-CMEndpointProtectionPoint.md)


