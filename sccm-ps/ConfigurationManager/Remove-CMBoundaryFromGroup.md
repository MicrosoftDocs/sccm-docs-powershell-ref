---
description: Removes a Configuration Manager boundary from a boundary group.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMBoundaryFromGroup
---

# Remove-CMBoundaryFromGroup

## SYNOPSIS
Removes a Configuration Manager boundary from a boundary group.

## SYNTAX

### RemoveBoundaryFromGroupById_Id (Default)
```
Remove-CMBoundaryFromGroup -BoundaryGroupId <Int32> -BoundaryId <Int32> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByName_Id
```
Remove-CMBoundaryFromGroup -BoundaryGroupId <Int32> -BoundaryName <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByObject_Id
```
Remove-CMBoundaryFromGroup -BoundaryGroupId <Int32> -BoundaryInputObject <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupById_Object
```
Remove-CMBoundaryFromGroup -BoundaryGroupInputObject <IResultObject> -BoundaryId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByName_Object
```
Remove-CMBoundaryFromGroup -BoundaryGroupInputObject <IResultObject> -BoundaryName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByObject_Object
```
Remove-CMBoundaryFromGroup -BoundaryGroupInputObject <IResultObject> -BoundaryInputObject <IResultObject>
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupById_Name
```
Remove-CMBoundaryFromGroup -BoundaryGroupName <String> -BoundaryId <Int32> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByName_Name
```
Remove-CMBoundaryFromGroup -BoundaryGroupName <String> -BoundaryName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByObject_Name
```
Remove-CMBoundaryFromGroup -BoundaryGroupName <String> -BoundaryInputObject <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMBoundaryFromGroup** cmdlet removes a Configuration Manager boundary from a boundary group.
A boundary is a network address range, subnet, or Active Directory site that identifies a group of computers that are close in the network.
A boundary group is a collection of boundaries.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a boundary from a group by using the boundary name
```
PS XYZ:\> Remove-CMBoundaryFromGroup -BoundaryGroupID "16777219" -BoundaryName "CLBound03"
```

This example removes a boundary named CLBound03 from a boundary group that has the ID 16777219.

### Example 2: Remove multiple boundary groups by using an InputObject
```
PS XYZ:\> $BoundaryObj = Get-CMBoundary -Name "Bound01", "Bound02", "Bound03"
PS XYZ:\> Remove-CMBoundaryFromGroup -Boundary $BoundaryObj -BoundaryGroupName "BGroup02"
```

The first command uses the **Get-CMBoundary** cmdlet to get multiple boundaries that are specified by their names, and stores this data into the **$BoundaryObj** variable.

The second command identifies and removes the boundaries that are specified by using the input object **$BoundaryObj**.
Because the *Force* parameter is not specified, you must confirm the action before it is performed.

## PARAMETERS

### -BoundaryGroupId
Specifies an ID for the boundary group from which you remove a boundary.

```yaml
Type: Int32
Parameter Sets: RemoveBoundaryFromGroupById_Id, RemoveBoundaryFromGroupByName_Id, RemoveBoundaryFromGroupByObject_Id
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
Parameter Sets: RemoveBoundaryFromGroupById_Object, RemoveBoundaryFromGroupByName_Object, RemoveBoundaryFromGroupByObject_Object
Aliases: BoundaryGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryGroupName
Specifies a name for the boundary group from which you remove a boundary.

```yaml
Type: String
Parameter Sets: RemoveBoundaryFromGroupById_Name, RemoveBoundaryFromGroupByName_Name, RemoveBoundaryFromGroupByObject_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryId
Specifies an ID for the boundary that this cmdlet removes.

```yaml
Type: Int32
Parameter Sets: RemoveBoundaryFromGroupById_Id, RemoveBoundaryFromGroupById_Object, RemoveBoundaryFromGroupById_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryInputObject
```yaml
Type: IResultObject
Parameter Sets: RemoveBoundaryFromGroupByObject_Id, RemoveBoundaryFromGroupByObject_Object, RemoveBoundaryFromGroupByObject_Name
Aliases: Boundary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryName
Specifies a name for the boundary that this cmdlet removes.

```yaml
Type: String
Parameter Sets: RemoveBoundaryFromGroupByName_Id, RemoveBoundaryFromGroupByName_Object, RemoveBoundaryFromGroupByName_Name
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

### -Force
Forces the command to run without asking for user confirmation.

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

## NOTES

## RELATED LINKS

[Add-CMBoundaryToGroup](Add-CMBoundaryToGroup.md)

[Get-CMBoundary](Get-CMBoundary.md)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[New-CMBoundary](New-CMBoundary.md)

[New-CMBoundaryGroup](New-CMBoundaryGroup.md)

[Remove-CMBoundary](Remove-CMBoundary.md)

[Remove-CMBoundaryGroup](Remove-CMBoundaryGroup.md)

[Set-CMBoundaryGroup](Set-CMBoundaryGroup.md)


