---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
schema: 2.0.0
title: Get-CMBoundaryGroup
---

# Get-CMBoundaryGroup

## SYNOPSIS

Get a boundary group.

## SYNTAX

### SearchByName (Default)
```
Get-CMBoundaryGroup [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBoundaryGroup -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use the **Get-CMBoundaryGroup** cmdlet to get a boundary group. A boundary group is a collection of boundaries.

You can use boundary groups to manage network locations. Before you can use the boundary group, assign boundaries to boundary groups .
Boundary groups enable client computers to find a primary site for client assignment, and a list of available site systems that have content.
For more information about boundaries, see [Overview of boundaries and boundary groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a boundary group that is specified by its name

This command gets a boundary group that is specified by the name **BGroup01**.

```powershell
Get-CMBoundaryGroup -Name "BGroup01"
```

### Example 2: Get multiple boundary groups that are specified by ID

This command gets multiple boundary groups that are specified by the identifiers `5` and `6`.

```powershell
Get-CMBoundaryGroup -Id 5,6
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

Specify an array of **group IDs** for one or more boundary groups. This value is an integer, for example `5`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name for a boundary group.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

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

### IResultObject[]#SMS_BoundaryGroup
### IResultObject#SMS_BoundaryGroup

## NOTES

For more information on this return object and its properties, see [SMS_BoundaryGroup server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_boundarygroup-server-wmi-class).

## RELATED LINKS

[New-CMBoundaryGroup](New-CMBoundaryGroup.md)

[Remove-CMBoundaryGroup](Remove-CMBoundaryGroup.md)

[Set-CMBoundaryGroup](Set-CMBoundaryGroup.md)

[Get-CMBoundaryGroupSiteSystem](Get-CMBoundaryGroupSiteSystem.md)

[Overview of boundaries and boundary groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups)
