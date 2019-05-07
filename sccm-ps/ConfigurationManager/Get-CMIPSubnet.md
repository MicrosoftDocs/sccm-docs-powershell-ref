---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 97B5236A-E4F2-4EA4-A45F-53F60F082705
online version: https://go.microsoft.com/fwlink/?linkid=833732
schema: 2.0.0
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
The **Get-CMIPSubnet** cmdlet gets an IP subnet object that Microsoft System Center Configuration Manager uses as a boundary.

A boundary is a network location on the intranet that can contain one or more devices that you want to manage.
Configuration Manager can define a boundary in several ways, including an IP subnet.
For more information about boundaries, see [Planning for Boundaries and Boundary Groups in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268431) on TechNet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get an IP subnet
```
PS XYZ:\> Get-CMIPSubnet -Name "West07Subnet"
```

This command gets the IP subnet object named West07Subnet.

## PARAMETERS

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
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMActiveDirectorySite](Get-CMActiveDirectorySite.md)


