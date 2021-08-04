---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
schema: 2.0.0
title: Get-CMBoundaryGroupRelationship
---

# Get-CMBoundaryGroupRelationship

## SYNOPSIS

Get a boundary group relationship.

## SYNTAX

### SearchByName (Default)
```
Get-CMBoundaryGroupRelationship [-DestinationGroupName <String>] [-SourceGroupName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMBoundaryGroupRelationship [-DestinationGroupId <Int32>] [-SourceGroupId <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the relationship between boundary groups. For more information, see [Configure boundary groups for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Get-CMBoundaryGroupRelationship -DestinationGroupName "Swindon" -SourceGroupName "London"
```

## PARAMETERS

### -DestinationGroupId

Specify the ID of the neighbor boundary group. This integer value is the **GroupID** property.

The destination boundary group can't be the same as the source boundary group.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationGroupName

Specify the name of the neighbor boundary group.

The destination boundary group can't be the same as the source boundary group.

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

### -SourceGroupId

Specify the ID of the boundary group that has the relationship. This integer value is the **GroupID** property.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceGroupName

Specify the name of the boundary group that has the relationship.

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

### IResultObject[]#SMS_BoundaryGroupRelationships
### IResultObject#SMS_BoundaryGroupRelationships

## NOTES

For more information on this return object and its properties, see [SMS_BoundaryGroupRelationships server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms-boundarygrouprelationships-server-wmi-class).

## RELATED LINKS

[New-CMBoundaryGroupRelationship](New-CMBoundaryGroupRelationship.md)

[Remove-CMBoundaryGroupRelationship](Remove-CMBoundaryGroupRelationship.md)

[Set-CMBoundaryGroupRelationship](Set-CMBoundaryGroupRelationship.md)

[Get-CMBoundaryGroupSiteSystem](Get-CMBoundaryGroupSiteSystem.md)

[Configure boundary groups for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups)
