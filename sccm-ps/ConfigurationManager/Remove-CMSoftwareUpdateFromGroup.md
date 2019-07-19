<<<<<<< HEAD
---
title: Remove-CMSoftwareUpdateFromGroup
titleSuffix: Configuration Manager
description: Removes a software update from group.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: 
schema: 2.0.0
>>>>>>> master
---

# Remove-CMSoftwareUpdateFromGroup

## SYNOPSIS
Removes a software update from group.

## SYNTAX

### ById_Id (Default)
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateId <String[]> -SoftwareUpdateGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById_Name
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateId <String[]> -SoftwareUpdateGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById_Object
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateId <String[]> -SoftwareUpdateGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Id
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateName <String[]> -SoftwareUpdateGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Name
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateName <String[]> -SoftwareUpdateGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName_Object
```
Remove-CMSoftwareUpdateFromGroup [-Force] -SoftwareUpdateName <String[]> -SoftwareUpdateGroup <IResultObject>
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

## DESCRIPTION
 

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1
```
PS XYZ:\>  
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
Parameter Sets: ById_Object, ByName_Object, ByObject_Object
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
Parameter Sets: ById_Id, ByName_Id, ByObject_Id
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
Parameter Sets: ById_Name, ByName_Name, ByObject_Name
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
Parameter Sets: ById_Id, ById_Name, ById_Object
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
Parameter Sets: ByName_Id, ByName_Name, ByName_Object
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]
Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

