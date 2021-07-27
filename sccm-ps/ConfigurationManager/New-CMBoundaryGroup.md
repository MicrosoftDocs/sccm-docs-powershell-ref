---
description: Creates a new boundary group.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMBoundaryGroup
---

# New-CMBoundaryGroup

## SYNOPSIS
Creates a new boundary group.

## SYNTAX

```
New-CMBoundaryGroup [-AddSiteSystemServer <IResultObject[]>] [-AddSiteSystemServerName <String[]>]
 [-DefaultSiteCode <String>] [-Description <String>] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMBoundaryGroup** cmdlet creates a new boundary group.
A boundary group is a collection of boundaries.

You can use boundary groups to manage network locations.
You must assign boundaries to boundary groups before you can use the boundary group.
Boundary groups enable client computers to find a primary site for client assignment, which is referred to as automatic site assignment, and a list of available site systems that have content.
For more information about boundaries, see [Planning for Boundaries and Boundary Groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups) and the [New-CMBoundary](New-CMBoundary.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a new boundary group

This example creates a new boundary group. After the new boundary group is created, the command displays an unpopulated list of boundary properties. To refresh and see a populated list, use the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

```powershell
New-CMBoundaryGroup -Name "BGroup05"
```

## PARAMETERS

### -AddSiteSystemServer
Specifies the site system server and link speed as the key/value pair in a hash table.
Valid values are:

- FastLink
- Slowlink

For example: @{"Server01.contoso.com" = "FastLink"}

**Important**: Starting in version 1610, FastLink is the only supported value for the hash table.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddSiteSystemServers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddSiteSystemServerName
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddSiteSystemServerNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSiteCode
Specifies the default site code for the boundary group.

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

### -Description
Specifies a description for the new boundary.

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

### -Name
Specifies a name for the new boundary.

```yaml
Type: String
Parameter Sets: (All)
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

### None
## OUTPUTS

### IResultObject#SMS_BoundaryGroup
## NOTES

## RELATED LINKS

[Define site boundaries and boundary groups for Configuration Manager](/sccm/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups#a-namebkmkboundarygroupsa-boundary-group/)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[Remove-CMBoundaryGroup](Remove-CMBoundaryGroup.md)

[Set-CMBoundaryGroup](Set-CMBoundaryGroup.md)

[New-CMBoundary](New-CMBoundary.md)
