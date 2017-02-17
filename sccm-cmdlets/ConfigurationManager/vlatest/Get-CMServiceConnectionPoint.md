---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833852
schema: 2.0.0
ms.assetid: 1A94F9DA-050E-442B-A30F-AD506DEDD42A
---

# Get-CMServiceConnectionPoint

## SYNOPSIS
Gets a service connection point.

## SYNTAX

### SearchByName
```
Get-CMServiceConnectionPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMServiceConnectionPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMServiceConnectionPoint** cmdlet gets a service connection point.

## EXAMPLES

### Example 1: Get a service connection point by name
```
PS C:\> Get-CMServiceConnectionPoint -SiteSystemServerName "TestServer01.Contoso.com" -SiteCode PS1
```

This command gets the service connection point for the site system server named TestServer01.Contoso.com with the site code PS1.

### Example 2: Get a service connection point by using a variable
```
PS C:\> $Server = Get-CMSiteSystemServer -SiteCode PS1 -SiteSystemServerName "TestServer02.Contoso.com"
PS C:\> Get-CMServiceConnectionPoint -InputObject $Server
```

The first command gets the site system server object named TestServer02.Contoso.com with the site code PS1 and saves the object in the $Server variable.

The second command gets the service connection point for the server stored in $Server.

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
Specifies a site system server object.
To obtain a site system server object, use the Get-CMSiteSystemServer cmdlet.

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
Specifies the name of a site system server that hosts the service connection point role.

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

[Add-CMServiceConnectionPoint](./Add-CMServiceConnectionPoint.md)

[Get-CMSiteSystemServer](./Get-CMSiteSystemServer.md)

[Remove-CMServiceConnectionPoint](./Remove-CMServiceConnectionPoint.md)

[Set-CMServiceConnectionPoint](./Set-CMServiceConnectionPoint.md)


