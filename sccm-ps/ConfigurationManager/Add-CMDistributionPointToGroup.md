---
description: Adds a distribution point to a distribution point group.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMDistributionPointToGroup
---

# Add-CMDistributionPointToGroup

## SYNOPSIS
Adds a distribution point to a distribution point group.

## SYNTAX

### AddDistributionPointToGroupByObject_Object (Default)
```
Add-CMDistributionPointToGroup -DistributionPoint <IResultObject> -DistributionPointGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByObject_Id
```
Add-CMDistributionPointToGroup -DistributionPoint <IResultObject> -DistributionPointGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByObject_Name
```
Add-CMDistributionPointToGroup -DistributionPoint <IResultObject> -DistributionPointGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupById_Object
```
Add-CMDistributionPointToGroup -DistributionPointGroup <IResultObject> -DistributionPointId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByName_Object
```
Add-CMDistributionPointToGroup -DistributionPointGroup <IResultObject> -DistributionPointName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupById_Id
```
Add-CMDistributionPointToGroup -DistributionPointGroupId <String> -DistributionPointId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByName_Id
```
Add-CMDistributionPointToGroup -DistributionPointGroupId <String> -DistributionPointName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupById_Name
```
Add-CMDistributionPointToGroup -DistributionPointGroupName <String> -DistributionPointId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByName_Name
```
Add-CMDistributionPointToGroup -DistributionPointGroupName <String> -DistributionPointName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDistributionPointToGroup** cmdlet adds a distribution point to a distribution point group.
Distribution point groups provide a logical grouping of distribution points for content distribution.

You can add one or more distribution points from any site in the Configuration Manager hierarchy to the distribution point group.
You can also add the distribution point to more than one distribution point group so that you can manage and monitor content from a central location for distribution points that span multiple sites.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a distribution point to a group
```
PS XYZ:\>Add-CMDistributionPointToGroup -DistributionPointGroupName "DPG01" -Id "{FA921CF2-89C9-407D-A21D-FE6947F2C00A}"
```

This command adds the distribution point that has the Id FA921CF2-89C9-407D-A21D-FE6947F2C00A to the distribution point group named DPG01.

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

### -DistributionPoint
Specifies a distribution point object.
To obtain a **CMDistributionPoint** object, use the [Get-CMDistributionPoint](Get-CMDistributionPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddDistributionPointToGroupByObject_Object, AddDistributionPointToGroupByObject_Id, AddDistributionPointToGroupByObject_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroup
Specifies a distribution point group object.
To obtain a **CMDistributionPointGroup** object, use the [Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddDistributionPointToGroupByObject_Object, AddDistributionPointToGroupById_Object, AddDistributionPointToGroupByName_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroupId
Specifies the ID of a distribution point group.

```yaml
Type: String
Parameter Sets: AddDistributionPointToGroupByObject_Id, AddDistributionPointToGroupById_Id, AddDistributionPointToGroupByName_Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
Specifies the name of a distribution point group.

```yaml
Type: String
Parameter Sets: AddDistributionPointToGroupByObject_Name, AddDistributionPointToGroupById_Name, AddDistributionPointToGroupByName_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointId
Specifies the ID of a distribution point.

```yaml
Type: String
Parameter Sets: AddDistributionPointToGroupById_Object, AddDistributionPointToGroupById_Id, AddDistributionPointToGroupById_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointName
Specifies the name of a distribution point.

```yaml
Type: String
Parameter Sets: AddDistributionPointToGroupByName_Object, AddDistributionPointToGroupByName_Id, AddDistributionPointToGroupByName_Name
Aliases:

Required: True
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

### System.Object
## NOTES

## RELATED LINKS

[Remove-CMDistributionPointFromGroup](Remove-CMDistributionPointFromGroup.md)

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)


