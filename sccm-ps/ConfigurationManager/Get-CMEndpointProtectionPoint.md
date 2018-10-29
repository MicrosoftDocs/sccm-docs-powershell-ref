---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 6B74ECA1-5193-46F2-8C2F-976B6E5D6EAD
online version: https://go.microsoft.com/fwlink/?linkid=833681
schema: 2.0.0
---

# Get-CMEndpointProtectionPoint

## SYNOPSIS
Gets an Endpoint Protection point.

## SYNTAX

### SearchByName (Default)
```
Get-CMEndpointProtectionPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-AllSite]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMEndpointProtectionPoint [-AllSite] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEndpointProtectionPoint** cmdlet gets a System Center 2016 Endpoint Protection point in Microsoft System Center Configuration Manager.
For more information about Endpoint Protection in Microsoft System Center Configuration Manager, see [Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427) on TechNet.

## EXAMPLES

### Example 1: Get an Endpoint Protection point
```
PS C:\> Get-CMEndpointProtectionPoint -SiteCode "CM1" -SiteSystemServerName "CMServer01.Contoso.com"
```

This command gets an Endpoint Protection point.

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

[Add-CMEndpointProtectionPoint](Add-CMEndpointProtectionPoint.md)

[Remove-CMEndpointProtectionPoint](Remove-CMEndpointProtectionPoint.md)

[Set-CMEndpointProtectionPoint](Set-CMEndpointProtectionPoint.md)


