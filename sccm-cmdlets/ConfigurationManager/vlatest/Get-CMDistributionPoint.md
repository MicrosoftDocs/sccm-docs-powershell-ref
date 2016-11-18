---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 590C1763-C913-4295-89D3-453ED1E32837
---

# Get-CMDistributionPoint

## SYNOPSIS
Gets a distribution point.

## SYNTAX

### SearchByName (Default)
```
Get-CMDistributionPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByGroupName
```
Get-CMDistributionPoint -DistributionPointGroupName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByGroupId
```
Get-CMDistributionPoint -DistributionPointGroupId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByGroup
```
Get-CMDistributionPoint -DistributionPointGroup <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMDistributionPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDistributionPoint** cmdlet gets a distribution point.

## EXAMPLES

### Example 1: Get a distribution point
```
PS C:\>Get-CMDistributionPoint -SiteSystemServerName "MySiteSys_11310.contoso.com"
```

This command gets the distribution point for the site system server named MySiteSys_11310.contoso.com.

### Example 2: Get a distribution point by using the pipeline
```
PS C:\>Get-CMDistributionPointGroup -Name "DPGroup" | Get-CMDistributionPoint
```

This command gets the distribution point group object named DPGroup and uses the pipeline operator to pass the object to **Get-CMDistributionPoint**, which gets all of the distribution points for the distribution point group object.

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

### -DistributionPointGroup
Specifies a distribution point group object.
To obtain a distribution point group object, use the Get-CMDistributionPointGroup cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroupId
Specifies the ID of a distribution point group.

```yaml
Type: String
Parameter Sets: SearchByGroupId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
Specifies the name of a distribution point group.

```yaml
Type: String
Parameter Sets: SearchByGroupName
Aliases: 

Required: True
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
Specifies the site code of the site that is associated with a distribution point.

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
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

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

[Add-CMDistributionPoint](./Add-CMDistributionPoint.md)

[Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md)

[Remove-CMDistributionPoint](./Remove-CMDistributionPoint.md)

[Set-CMDistributionPoint](./Set-CMDistributionPoint.md)

[Update-CMDistributionPoint](./Update-CMDistributionPoint.md)

[Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md)


