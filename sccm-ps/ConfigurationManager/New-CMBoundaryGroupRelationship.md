---
description: Create a boundary group relationship.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2020
schema: 2.0.0
title: New-CMBoundaryGroupRelationship
---

# New-CMBoundaryGroupRelationship

## SYNOPSIS

Create a boundary group relationship.

## SYNTAX

### NameMandatory (Default)
```
New-CMBoundaryGroupRelationship -DestinationGroupName <String> [-FallbackDPMinutes <Int32>]
 [-FallbackMPMinutes <Int32>] [-FallbackSmpMinutes <Int32>] [-FallbackSupMinutes <Int32>]
 -SourceGroupName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValueMandatory
```
New-CMBoundaryGroupRelationship -DestinationGroup <IResultObject> [-FallbackDPMinutes <Int32>]
 [-FallbackMPMinutes <Int32>] [-FallbackSmpMinutes <Int32>] [-FallbackSupMinutes <Int32>]
 -SourceGroup <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### IdMandatory
```
New-CMBoundaryGroupRelationship -DestinationGroupId <Int32> [-FallbackDPMinutes <Int32>]
 [-FallbackMPMinutes <Int32>] [-FallbackSmpMinutes <Int32>] [-FallbackSupMinutes <Int32>]
 -SourceGroupId <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a relationship between boundary groups. Boundary groups that you link together are called _neighbor_ boundary groups. A boundary group can have more than one relationship, each with a specific neighbor boundary group.

When a client fails to find an available site system in its current boundary group, the configuration of each relationship determines when it begins to search a neighbor boundary group. This search of other groups is called _fallback_.

For more information, see [Configure boundary groups for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a relationship for only content

This command creates a relationship between the **Swindon** and **London** boundary groups. Distribution points fall back after five minutes. Software update points and management points never fall back.

```powershell
New-CMBoundaryGroupRelationship -SourceGroupName "Swindon" -DestinationGroupName "London" -FallbackDPMinutes 5 -FallbackSupMinutes -1 -FallbackMPMinutes -1
```

## PARAMETERS

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationGroup

Specify a boundary group object for the neighbor. To get this object, use the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

The destination boundary group can't be the same as the source boundary group.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationGroupId

Specify the ID of the neighbor boundary group. This integer value is the **GroupID** property.

The destination boundary group can't be the same as the source boundary group.

```yaml
Type: Int32
Parameter Sets: IdMandatory
Aliases:

Required: True
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
Parameter Sets: NameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

### -FallbackDPMinutes

Specify an integer value for the fallback time in minutes for distribution points (DP) from the source to the destination boundary group. To set the option to **Never fallback**, specify the value `-1`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FallbackMPMinutes

Specify an integer value for the fallback time in minutes for management points (MP) from the source to the destination boundary group. To set the option to **Never fallback**, specify the value `-1`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FallbackSmpMinutes

Specify an integer value for the fallback time in minutes for state migration points (SMP) from the source to the destination boundary group. To set the option to **Never fallback**, specify the value `-1`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FallbackSupMinutes

Specify an integer value for the fallback time in minutes for software update points (SUP) from the source to the destination boundary group. To set the option to **Never fallback**, specify the value `-1`.

```yaml
Type: Int32
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

### -SourceGroup

Specify a boundary group object from which to create the relationship. To get this object, use the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceGroupId

Specify the ID of the boundary group from which to create the relationship. This integer value is the **GroupID** property.

```yaml
Type: Int32
Parameter Sets: IdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceGroupName

Specify the name of the boundary group from which to create the relationship.

```yaml
Type: String
Parameter Sets: NameMandatory
Aliases:

Required: True
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_BoundaryGroupRelationships

## NOTES

## RELATED LINKS

[Get-CMBoundaryGroupRelationship](Get-CMBoundaryGroupRelationship.md)

[Remove-CMBoundaryGroupRelationship](Remove-CMBoundaryGroupRelationship.md)

[Set-CMBoundaryGroupRelationship](Set-CMBoundaryGroupRelationship.md)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[Configure boundary groups for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups)
