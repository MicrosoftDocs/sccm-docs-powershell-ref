---
description: Removes a software update from group.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMSoftwareUpdateFromGroup
---

# Remove-CMSoftwareUpdateFromGroup

## SYNOPSIS
Removes a software update from group.

## SYNTAX

### ById_Id (Default)
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateGroupId <String> -SoftwareUpdateId <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject_Id
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdate <IResultObject[]> -SoftwareUpdateGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject_Name
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdate <IResultObject[]> -SoftwareUpdateGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObject_Object
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdate <IResultObject[]>
 -SoftwareUpdateGroup <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById_Object
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateGroup <IResultObject> -SoftwareUpdateId <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Object
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateGroup <IResultObject> -SoftwareUpdateName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Id
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateGroupId <String> -SoftwareUpdateName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById_Name
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateGroupName <String> -SoftwareUpdateId <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Name
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateGroupName <String> -SoftwareUpdateName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

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

### -Force
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

### -SoftwareUpdate
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
```yaml
Type: String[]
Parameter Sets: ByName_Object, ByName_Id, ByName_Name
Aliases: SoftwareUpdateNames

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
Default value: None
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
