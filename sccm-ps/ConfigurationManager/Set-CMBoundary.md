---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/14/2021
schema: 2.0.0
title: Set-CMBoundary
---

# Set-CMBoundary

## SYNOPSIS

Configure a site boundary.

## SYNTAX

### SetByValue (Default)
```
Set-CMBoundary -InputObject <IResultObject> [-NewName <String>] [-NewType <BoundaryTypes>] [-NewValue <String>]
 [-PassThru] [-ValueStartsWith <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMBoundary -Id <String> [-NewName <String>] [-NewType <BoundaryTypes>] [-NewValue <String>] [-PassThru]
 [-ValueStartsWith <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMBoundary [-NewName <String>] [-NewType <BoundaryTypes>] [-NewValue <String>] [-PassThru]
 -Type <BoundaryTypes> -Value <String> [-ValueStartsWith <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure a site boundary. A boundary is a network location that contains one or more devices that you can manage. A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, an IP address range, or a VPN. For more information, see [Define site boundaries and boundary groups](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a boundary

This command changes a boundary name from Default-ADSite to ADSiteBoundary01.

```powershell
Set-CMBoundary -Name "Default-ADSite" -NewName "ADSiteBoundary01"
```

### Example 2: Modify the value of a boundary by using an InputObject

In this example, the first command gets a boundary that has the ID of 16777217 and inserts it into the input object $BoundaryObj.

The second command identifies the boundary by using the input object $BoundaryObj and modifies its value to IPSubnet17.

```powershell
$BoundaryObj = Get-CMBoundary -Id "16777217"
Set-CMBoundary -InputObject $BoundaryObj -Value "IPSubnet17"
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

### -Id

Specify a boundary identifier (ID) to modify. This value is an integer, for example `26`.

```yaml
Type: String
Parameter Sets: SetById
Aliases: BoundaryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a boundary object to modify. To get this object, use the [Get-CMBoundary](Get-CMBoundary.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NewName

Specify a new name for a boundary.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DisplayName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewType

Specify the boundary type.

```yaml
Type: BoundaryTypes
Parameter Sets: (All)
Aliases: NewBoundaryType
Accepted values: IPSubnet, ADSite, IPV6Prefix, IPRange, Vpn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewValue

Specify the data that defines the boundary. For example, an Active Directory site value can be `Default-First-Site-Name`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -Type

Specify a boundary type.

```yaml
Type: BoundaryTypes
Parameter Sets: SetByName
Aliases: BoundaryType
Accepted values: IPSubnet, ADSite, IPV6Prefix, IPRange, Vpn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

Specify the data that describes the boundary.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueStartsWith

Set this parameter to `$true` to match the start of a connection name or description instead of the whole string. For more information, see [Define network locations as boundaries](/mem/configmgr/core/servers/deploy/configure/boundaries#vpn).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_Boundary

## NOTES

For more information on this return object and its properties, see [SMS_Boundary server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_boundary-server-wmi-class).

## RELATED LINKS

[Get-CMBoundary](Get-CMBoundary.md)

[New-CMBoundary](New-CMBoundary.md)

[Remove-CMBoundary](Remove-CMBoundary.md)
