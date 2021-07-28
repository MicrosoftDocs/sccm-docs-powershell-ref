---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/26/2021
schema: 2.0.0
title: New-CMBoundary
---

# New-CMBoundary

## SYNOPSIS

Create a site boundary.

## SYNTAX

```
New-CMBoundary [-Name <String>] -Type <BoundaryTypes> -Value <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a site boundary. A boundary is a network location that contains one or more devices that you can manage. A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, an IP address range, or a VPN. For more information, see [Define site boundaries and boundary groups](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create an IP subnet site boundary

This command creates a new IP subnet site boundary that has a name of **IPSubNetBoundary01** and a value of **172.16.50.0/24**.

```powershell
New-CMBoundary -DisplayName "IPSubNetBoundary01" -BoundaryType IPSubNet -Value "172.16.50.0/24"
```

### Example 2: Create an Active Directory site boundary

This command creates a new Active Directory site boundary that has a name of **ADSiteBoundary01** and a value of **Default-First-Site-Name**.

```powershell
New-CMBoundary -DisplayName "ADSiteBoundary01" -BoundaryType ADSite -Value "Default-First-Site-Name"
```

### Example 3: Create an IPv6 prefix site boundary

This command creates a new IPv6 prefix site boundary that has a name of **IPv6PrefixBoundary01** and a value of **FE80::/64**.

```powershell
New-CMBoundary -DisplayName "IPv6PrefixBoundary01" -BoundaryType IPv6Prefix -Value "FE80::/64"
```

### Example 4: Create an IP range site boundary

This command creates a new IP range site boundary that has the name **IPRangeBoundary01** and a value of **10.255.255.0-10.255.255.255**.

```powershell
New-CMBoundary -DisplayName "IPRangeBoundary01" -BoundaryType IPRange -Value "10.255.255.0-10.255.255.255"
```

### Example 5: Create a VPN site boundary

This command creates a new VPN site boundary that has the name **VPN-CONTOSO1-Name** and a value of **Name:CONTOSO1**.

```powershell
New-CMBoundary -DisplayName "VPN-CONTOSO1-Name" -BoundaryType VPN -Value "Name:CONTOSO1"
```

## PARAMETERS

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

Specify the name of the new boundary.

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

Specify the boundary type.

```yaml
Type: BoundaryTypes
Parameter Sets: (All)
Aliases: BoundaryType
Accepted values: IPSubnet, ADSite, IPV6Prefix, IPRange, Vpn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

Specify the data that defines the boundary. For example, an Active Directory site value can be `Default-First-Site-Name`.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject#SMS_Boundary
## NOTES

For more information on this return object and its properties, see [SMS_Boundary server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_boundary-server-wmi-class).

## RELATED LINKS

[Get-CMBoundary](Get-CMBoundary.md)

[Remove-CMBoundary](Remove-CMBoundary.md)

[Set-CMBoundary](Set-CMBoundary.md)
