---
description: Gets a boundary group.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMBoundaryGroup
---

# Get-CMBoundaryGroup

## SYNOPSIS
Gets a boundary group.

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
The **Get-CMBoundaryGroup** cmdlet gets a boundary group.
A boundary group is a collection of boundaries.

You can use boundary groups to manage network locations.
You must assign boundaries to boundary groups before you can use the boundary group.
Boundary groups enable client computers to find a primary site for client assignment, which is referred to as automatic site assignment, and a list of available site systems that have content.
For more information about boundaries, see [Planning for Boundaries and Boundary Groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a boundary group that is specified by its identifier
```
PS XYZ:\> Get-CMBoundaryGroup -Id "1600231"
CreatedBy:          Contoso\ENarvaez
CreatedOn           5/17/2012 06:01:29 AM
DefaultSiteCode:
Description:
GroupID:            1600231
MemberCount:        80
ModifiedBy:
ModifiedOn:
Name:               BGroup01
SiteSystemCount:    0
```

This command gets a boundary group that is specified by the identifier 1600231.

### Example 2: Get multiple boundary groups that are specified by name
```
PS XYZ:\> Get-CMBoundaryGroup -Name "BGroup01", "BGroup02", "BGroup03"
CreatedBy:          Contoso\ENarvaez
CreatedOn           5/17/2012 07:13:02 AM
DefaultSiteCode:
Description:
GroupID:            1600231
MemberCount:        80
ModifiedBy:
ModifiedOn:
Name:               BGroup01
SiteSystemCount:    0
CreatedBy:          Contoso\ENarvaez
CreatedOn           7/13/2012 12:24:21 PM
DefaultSiteCode:
Description:
GroupID:            1600246
MemberCount:        11
ModifiedBy:         Contoso\DChew
ModifiedOn:         9/10/2012 04:32:16 PM
Name:               BGroup02
SiteSystemCount:    0
CreatedBy:          Contoso\DChew
CreatedOn           8/06/2012 09:32:05 AM
DefaultSiteCode:
Description:
GroupID:            1600249
MemberCount:        96
ModifiedBy:         Contoso\EDaugherty
ModifiedOn:         9/14/2012 10:11:36 AM
Name:               BGroup03
SiteSystemCount:    0
```

This command gets multiple boundary groups that are specified by the names BGroup01, BGroup02, and BGroup03.

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
Specifies an array of identifiers (IDs) for one or more boundary groups.

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
Specifies the name for a boundary group.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_BoundaryGroup

### IResultObject#SMS_BoundaryGroup

## NOTES

## RELATED LINKS

[Planning for Boundaries and Boundary Groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups)

[New-CMBoundaryGroup](New-CMBoundaryGroup.md)

[Remove-CMBoundaryGroup](Remove-CMBoundaryGroup.md)

[Set-CMBoundaryGroup](Set-CMBoundaryGroup.md)


