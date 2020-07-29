---
description: Modifies Configuration Manager boundary settings.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMBoundary
---

# Set-CMBoundary

## SYNOPSIS
Modifies Configuration Manager boundary settings.

## SYNTAX

### SetByValue (Default)
```
Set-CMBoundary [-NewName <String>] -InputObject <IResultObject> [-NewType <BoundaryTypes>] [-NewValue <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMBoundary -Id <String> [-NewName <String>] [-NewType <BoundaryTypes>] [-NewValue <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMBoundary [-NewName <String>] -Type <BoundaryTypes> -Value <String> [-NewType <BoundaryTypes>]
 [-NewValue <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMBoundary** cmdlet modifies boundary settings.

In Microsoft System Center Configuration Manager, a boundary is an intranet location that contains one or more devices that you can manage.
A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, or an IP address range.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Rename a boundary
```
PS XYZ:\> Set-CMBoundary -Name "Default-ADSite" -NewName "ADSiteBoundary01"
```

This command changes a boundary name from Default-ADSite to ADSiteBoundary01.

### Example 2: Modify the value of a boundary by using an InputObject
```
PS XYZ:\> $BoundaryObj = Get-CMBoundary -Id "16777217"
PS XYZ:\> Set-CMBoundary -InputObject $BoundaryObj -Value "IPSubnet17"
```

In this example, the first command gets a boundary that has the ID of 16777217 and inserts it into the input object $BoundaryObj.

The second command identifies the boundary by using the input object $BoundaryObj and modifies its value to IPSubnet17.

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
Specifies an array of boundary identifiers (IDs).

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
Specifies an input object to this cmdlet.
You can get the input object by using the Get-CMBoundary cmdlet.

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
Specifies a new name for a boundary.

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
{{ Fill NewType Description }}

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
{{ Fill NewValue Description }}

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
Returns the current working object.
By default, this cmdlet does not generate any output.

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
Specifies a boundary type.
Valid values are: ADSite, IPV6Prefix, IPSubnet, and IPRange.

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
Specifies the data that describes the boundary.
For example, an Active Directory site value can be Default-ADSite.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_Boundary

## NOTES

## RELATED LINKS

[Get-CMBoundary](Get-CMBoundary.md)

[New-CMBoundary](New-CMBoundary.md)

[Remove-CMBoundary](Remove-CMBoundary.md)


