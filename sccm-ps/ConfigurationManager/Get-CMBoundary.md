---
description: Gets a Configuration Manager boundary.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMBoundary
---

# Get-CMBoundary

## SYNOPSIS
Gets a Configuration Manager boundary.

## SYNTAX

### SearchByName (Default)
```
Get-CMBoundary [-BoundaryName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBoundary -BoundaryId <UInt32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByBoundaryGroupIdMandatory
```
Get-CMBoundary -BoundaryGroupId <UInt32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByBoundaryGroupNameMandatory
```
Get-CMBoundary -BoundaryGroupName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByBoundaryGroup
```
Get-CMBoundary -BoundaryGroupInputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBoundary** cmdlet gets a System Center Configuration Manager boundary.

In Microsoft System Center Configuration Manager, a boundary is an intranet location that contains one or more devices that you can manage.
A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, or an IP address range.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a boundary that is specified by its identifier
```
PS XYZ:\> Get-Boundary -Id "67777217"
BoundaryFlags:      0
BoundaryID:         67777217
BoundaryType:       1
CreatedBy:          Contoso\PFuller
CreatedOn           6/10/2012 2:58:56 PM
DefaultSiteCode:
DisplayName:
GroupCount:         0
ModifiedBy:         Contoso\PFuller
ModifiedOn:         9/13/2012  10:04 AM
SiteSystems:
Value:              Default1
```

This command gets a boundary that is specified by the identifier 67777217.

### Example 2: Get a boundary that is specified by the name of an associated boundary group
```
PS XYZ:\> Get-Boundary -BoundaryGroupName "BGroup07"
BoundaryFlags:      0
BoundaryID:         63997411
BoundaryType:       2
CreatedBy:          Contoso\PFuller
CreatedOn           4/13/2012 06:58:56 AM
DefaultSiteCode:
DisplayName:
GroupCount:         1
ModifiedBy:         Contoso\PFuller
ModifiedOn:         8/02/2012  11:16 AM
SiteSystems:
Value:              Default1
```

This command gets a boundary that is specified by the associated boundary group BGroup07.

## PARAMETERS

### -BoundaryGroupId
Specifies an identifier (ID) for a boundary group.
You can get a boundary group ID by using the **Get-CMBoundaryGroup** cmdlet.

```yaml
Type: UInt32
Parameter Sets: SearchByBoundaryGroupIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryGroupInputObject
```yaml
Type: IResultObject
Parameter Sets: SearchByBoundaryGroup
Aliases: BoundaryGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryGroupName
Specifies a name for a boundary group.
You can get a boundary group name by using the **Get-CMBoundaryGroup** cmdlet.

```yaml
Type: String
Parameter Sets: SearchByBoundaryGroupNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryId
```yaml
Type: UInt32
Parameter Sets: SearchByIdMandatory
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryName
```yaml
Type: String
Parameter Sets: SearchByName
Aliases: DisplayName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Remove-CMBoundary](Remove-CMBoundary.md)

[New-CMBoundary](New-CMBoundary.md)

[Set-CMBoundary](Set-CMBoundary.md)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)
