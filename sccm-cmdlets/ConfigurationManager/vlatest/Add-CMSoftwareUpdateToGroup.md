---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833761
schema: 2.0.0
ms.assetid: 86BEA428-375A-470C-8F80-36DA8B5626A9
---

# Add-CMSoftwareUpdateToGroup

## SYNOPSIS
Adds a software update to a software update group in Configuration Manager.

## SYNTAX

### AddSoftwareUpdateToGroupById_Id (Default)
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateId <String[]> -SoftwareUpdateGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddSoftwareUpdateToGroupById_Name
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateId <String[]> -SoftwareUpdateGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddSoftwareUpdateToGroupById_Object
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateId <String[]> -SoftwareUpdateGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddSoftwareUpdateToGroupByName_Id
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateName <String[]> -SoftwareUpdateGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddSoftwareUpdateToGroupByName_Name
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateName <String[]> -SoftwareUpdateGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddSoftwareUpdateToGroupByName_Object
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdateName <String[]> -SoftwareUpdateGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddSoftwareUpdateToGroupByObject_Name
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdate <IResultObject[]> -SoftwareUpdateGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddSoftwareUpdateToGroupByObject_Object
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdate <IResultObject[]> -SoftwareUpdateGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddSoftwareUpdateToGroupByObject_Id
```
Add-CMSoftwareUpdateToGroup -SoftwareUpdate <IResultObject[]> -SoftwareUpdateGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMSoftwareUpdateToGroup** cmdlet adds a software update to a software update group in Microsoft System Center Configuration Manager.
You can specify a software update by name or by ID or use the [Get-CMSoftwareUpdate](./Get-CMSoftwareUpdate.md) cmdlet to obtain an update.
Likewise, you can specify a software update group by name or by ID or use the [Get-CMSoftwareUpdateGroup](./Get-CMSoftwareUpdateGroup.md) cmdlet to obtain one.

## EXAMPLES

### Example 1: Add an update to a software group
```
PS C:\>Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroupName "Accounting Group updates" -SoftwareUpdateId "SMS00078"
```

This command adds a software update with the ID SMS00078 to the update group named Accounting Group updates.

### Example 2: Add an update to a software group by using IDs
```
PS C:\>Add-CMSoftwareUpdateToGroup -SoftwareUpdateGroupId "SUP00045" -SoftwareUpdateId "SMS00078"
```

This command adds a software update that has the ID SMS00078 to the update group with the specified ID.

## PARAMETERS

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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
Parameter Sets: AddSoftwareUpdateToGroupByObject_Name, AddSoftwareUpdateToGroupByObject_Object, AddSoftwareUpdateToGroupByObject_Id
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
Parameter Sets: AddSoftwareUpdateToGroupById_Object, AddSoftwareUpdateToGroupByName_Object, AddSoftwareUpdateToGroupByObject_Object
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
Parameter Sets: AddSoftwareUpdateToGroupById_Id, AddSoftwareUpdateToGroupByName_Id, AddSoftwareUpdateToGroupByObject_Id
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
Parameter Sets: AddSoftwareUpdateToGroupById_Name, AddSoftwareUpdateToGroupByName_Name, AddSoftwareUpdateToGroupByObject_Name
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
Parameter Sets: AddSoftwareUpdateToGroupById_Id, AddSoftwareUpdateToGroupById_Name, AddSoftwareUpdateToGroupById_Object
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
Parameter Sets: AddSoftwareUpdateToGroupByName_Id, AddSoftwareUpdateToGroupByName_Name, AddSoftwareUpdateToGroupByName_Object
Aliases: SoftwareUpdateNames
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdate](./Get-CMSoftwareUpdate.md)

[Get-CMSoftwareUpdateGroup](./Get-CMSoftwareUpdateGroup.md)


