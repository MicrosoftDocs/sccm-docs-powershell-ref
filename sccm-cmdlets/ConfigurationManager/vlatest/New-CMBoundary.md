---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 5457BE35-1591-44A8-8D2E-6624532F633D
---

# New-CMBoundary

## SYNOPSIS
Creates a boundary.

## SYNTAX

```
New-CMBoundary [-Name <String>] -Type <BoundaryTypes> -Value <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMBoundary** cmdlet creates a boundary.

In Microsoft System Center Configuration Manager, a boundary is an intranet location that contains one or more devices that you can manage.
A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, or an IP address range.

## EXAMPLES

### Example 1: Create a new IP Subnet site boundary
```
PS C:\>New-CMBoundary -DisplayName "IPSubNetBoundary01" -BoundaryType IPSubNet -Value "172.16.50.0/24"
BoundaryFlags:      0
BoundaryID:         6338009
BoundaryType:       0
CreatedBy:          Contoso\PFuller
CreatedOn           6/10/2012 1:17:42 PM
DefaultSiteCode: 
DisplayName:        IPSubNetBoundary01
GroupCount:         0
ModifiedBy:         
ModifiedOn:         
SiteSystems: 
Value:              172.16.50.0/24
```

This command creates a new IP subnet site boundary that has a name of IPSubNetBoundary01 and a value of 172.16.50.0/24.

### Example 2: Create a new Active Directory site boundary
```
PS C:\>New-CMBoundary -DisplayName "ADSiteBoundary01" -BoundaryType ADSite -Value "Default-First-Site-Name"
BoundaryFlags:      0
BoundaryID:         6339999
BoundaryType:       1
CreatedBy:          Contoso\PFuller
CreatedOn           6/10/2012 2:58:56 PM
DefaultSiteCode: 
DisplayName:        ADSiteBoundary01
GroupCount:         0
ModifiedBy:          
SiteSystems: 
Value:              Default-First-Site-Name
```

This command creates a new Active Directory site boundary that has a name of ADSiteBoundary01 and a value of Default-First-Site-Name.

### Example 3: Create a new IP v6 prefix site boundary
```
PS C:\>New-CMBoundary -DisplayName "IPv6PrefixBoundary01" -BoundaryType IPv6Prefix -Value "FE80::/64".
BoundaryFlags:      0
BoundaryID:         63347110
BoundaryType:       2
CreatedBy:          Contoso\PFuller
CreatedOn           6/10/2012 3:15:19 PM
DefaultSiteCode: 
DisplayName:        IPv6PrefixBoundary01
GroupCount:         0
ModifiedBy:         
ModifiedOn:         
SiteSystems: 
Value:              "FE80::/64"
```

This command creates a new IP v6 prefix site boundary that has a name of IPv6PrefixBoundary01 and a value of FE80::/64.

### Example 4: Create a new IP range site boundary
```
PS C:\>New-CMBoundary -DisplayName "IPRangeBoundary01" -BoundaryType IPRange -Value "10.255.255.0-10.255.255.255" 
BoundaryFlags:      0
BoundaryID:         6334129
BoundaryType:       3
CreatedBy:          Contoso\PFuller
CreatedOn           6/10/2012 3:29:05 PM
DefaultSiteCode: 
DisplayName:        IPRangeBoundary01
GroupCount:         0
ModifiedBy:         
ModifiedOn:         
SiteSystems: 
Value:              10.255.255.0-10.255.255.255
```

This command creates a new IP range site boundary that has the name IPRangeBoundary01 and a value of 10.255.255.0-10.255.255.255.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Name


```yaml
Type: String
Parameter Sets: (All)
Aliases: DisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type


```yaml
Type: BoundaryTypes
Parameter Sets: (All)
Aliases: BoundaryType
Accepted values: IPSubnet, ADSite, IPV6Prefix, IPRange

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMBoundary](./Get-CMBoundary.md)

[Remove-CMBoundary](./Remove-CMBoundary.md)

[Set-CMBoundary](./Set-CMBoundary.md)


