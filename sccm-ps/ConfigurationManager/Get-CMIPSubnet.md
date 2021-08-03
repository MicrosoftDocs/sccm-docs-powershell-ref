---
description: Gets a Configuration Manager IP subnet.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMIPSubnet
---

# Get-CMIPSubnet

## SYNOPSIS
Gets a Configuration Manager IP subnet.

## SYNTAX

### SearchByName (Default)
```
Get-CMIPSubnet [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMIPSubnet -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMIPSubnet** cmdlet gets an IP subnet object that Configuration Manager uses as a boundary.

A boundary is a network location on the intranet that can contain one or more devices that you want to manage.
Configuration Manager can define a boundary in several ways, including an IP subnet.
For more information about boundaries, see [Planning for Boundaries and Boundary Groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an IP subnet
```
PS XYZ:\> Get-CMIPSubnet -Name "West07Subnet"
```

This command gets the IP subnet object named West07Subnet.

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

### -Id
Specifies an array of IDs for IP subnets.
This is a Configuration Manager name, not an IP address or IP address and subnet.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: SubnetId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names for IP subnets.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ADSubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_ADSubnet
### IResultObject#SMS_ADSubnet
## NOTES

## RELATED LINKS

[Get-CMActiveDirectorySite](Get-CMActiveDirectorySite.md)


