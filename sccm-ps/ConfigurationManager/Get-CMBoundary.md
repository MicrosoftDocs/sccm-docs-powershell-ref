---
description: Get a site boundary.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/26/2020
schema: 2.0.0
title: Get-CMBoundary
---

# Get-CMBoundary

## SYNOPSIS

Get a site boundary.

## SYNTAX

### SearchByName (Default)
```
Get-CMBoundary [-BoundaryName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByBoundaryGroupIdMandatory
```
Get-CMBoundary -BoundaryGroupId <UInt32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByBoundaryGroup
```
Get-CMBoundary -BoundaryGroupInputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByBoundaryGroupNameMandatory
```
Get-CMBoundary -BoundaryGroupName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBoundary -BoundaryId <UInt32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMBoundary** cmdlet gets a Configuration Manager boundary.

In Configuration Manager, a boundary is a network location that contains one or more devices that you can manage.
A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, IP address range, or VPN.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a boundary by its ID

This command gets a boundary that's specified by the ID **67777217**.

```powershell
PS XYZ:\> Get-CMBoundary -Id "67777217"
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

### Example 2: Get a boundary by the name of an associated boundary group

This command gets a boundary that's specified by the associated boundary group **BGroup07**.

```powershell
Get-CMBoundary -BoundaryGroupName "BGroup07"
```

## PARAMETERS

### -BoundaryGroupId

Specify the ID of a boundary group that includes the boundary to get. You can get a boundary group ID by using the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet. This ID is the **GroupID** property on the [SMS_BoundaryGroup](/mem/configmgr/develop/reference/core/servers/configure/sms_boundarygroup-server-wmi-class) object. For example, `33`.

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

Specify an object for a boundary group that includes the boundary to get. You can get this object by using the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

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

Specify the name of a boundary group that includes the boundary to get.

```yaml
Type: String
Parameter Sets: SearchByBoundaryGroupNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -BoundaryId

Specify the ID of the boundary to get. This ID is the **BoundaryID** property on the [SMS_Boundary](/mem/configmgr/develop/reference/core/servers/configure/sms_boundary-server-wmi-class) object. For example, `23`.

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

Specify the name of the boundary to get. This name is the **DisplayName** property on the [SMS_Boundary](/mem/configmgr/develop/reference/core/servers/configure/sms_boundary-server-wmi-class) object.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: DisplayName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_Boundary
### IResultObject#SMS_Boundary
## NOTES

## RELATED LINKS

[Remove-CMBoundary](Remove-CMBoundary.md)

[New-CMBoundary](New-CMBoundary.md)

[Set-CMBoundary](Set-CMBoundary.md)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[Define site boundaries and boundary groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups)
