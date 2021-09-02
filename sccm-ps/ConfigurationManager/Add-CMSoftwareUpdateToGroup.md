---
description: Adds a software update to a software update group in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMSoftwareUpdateToGroup
---

# Add-CMSoftwareUpdateToGroup

## SYNOPSIS
Adds a software update to a software update group in Configuration Manager.

## SYNTAX

### ById_Id (Default)
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroupId <String> -SoftwareUpdateId <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject_Id
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdate <IResultObject[]> -SoftwareUpdateGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject_Name
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdate <IResultObject[]> -SoftwareUpdateGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject_Object
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdate <IResultObject[]> -SoftwareUpdateGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById_Object
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroup <IResultObject> -SoftwareUpdateId <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Object
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroup <IResultObject> -SoftwareUpdateName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Id
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroupId <String> -SoftwareUpdateName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById_Name
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroupName <String> -SoftwareUpdateId <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Name
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroupName <String> -SoftwareUpdateName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMSoftwareUpdateToGroup** cmdlet adds a software update to a software update group in Configuration Manager.
You can specify a software update by name or by ID or use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet to obtain an update.
Likewise, you can specify a software update group by name or by ID or use the [Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md) cmdlet to obtain one.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add an update to a software group
```
PS XYZ:\>Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroupName "Accounting Group updates" -SoftwareUpdateId "SMS00078"
```

This command adds a software update with the ID SMS00078 to the update group named Accounting Group updates.

### Example 2: Add an update to a software group by using IDs
```
PS XYZ:\>Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroupId "SUP00045" -SoftwareUpdateId "SMS00078"
```

This command adds a software update that has the ID SMS00078 to the update group with the specified ID.

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

### -SoftwareUpdate
Specifies a software update object.
To obtain a software update object, use **Get-CMSoftwareUpdate**.

```yaml
Type: IResultObject[]
Parameter Sets: ByObject_Id, ByObject_Name, ByObject_Object
Aliases: SoftwareUpdates

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroup
Specifies a software update group object.
To obtain a software update group object, use **Get-CMSoftwareUpdateGroup**.

```yaml
Type: IResultObject
Parameter Sets: ByObject_Object, ById_Object, ByName_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId
Specifies an ID of a software group.

```yaml
Type: String
Parameter Sets: ById_Id, ByObject_Id, ByName_Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName
Specifies a name of a software group.

```yaml
Type: String
Parameter Sets: ByObject_Name, ById_Name, ByName_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateId
Specifies an ID of a software update.

```yaml
Type: String[]
Parameter Sets: ById_Id, ById_Object, ById_Name
Aliases: SoftwareUpdateIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName
Specifies a name of a software update.

```yaml
Type: String[]
Parameter Sets: ByName_Object, ByName_Id, ByName_Name
Aliases: SoftwareUpdateNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]
### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)


