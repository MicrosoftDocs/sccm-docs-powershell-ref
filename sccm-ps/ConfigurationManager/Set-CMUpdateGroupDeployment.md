---
author: aczechowski
description: Sets an update group deployment.
external help file: AdminUI.PS.Deployments.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMUpdateGroupDeployment
titleSuffix: Configuration Manager
---

# Set-CMUpdateGroupDeployment

## SYNOPSIS
Sets an update group deployment.

## SYNTAX

### ByValueEnable (Default)
```
Set-CMUpdateGroupDeployment [-Enable] -UpdateGroupDeployment <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameDisable
```
Set-CMUpdateGroupDeployment [-Disable] [-DeploymentName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdDisable
```
Set-CMUpdateGroupDeployment [-Disable] -UpdateGroupDeploymentId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueDisable
```
Set-CMUpdateGroupDeployment [-Disable] -UpdateGroupDeployment <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDeploymentSummaryValueDisable
```
Set-CMUpdateGroupDeployment [-Disable] -Deployment <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameEnable
```
Set-CMUpdateGroupDeployment [-Enable] [-DeploymentName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdEnable
```
Set-CMUpdateGroupDeployment [-Enable] -UpdateGroupDeploymentId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDeploymentSummaryValueEnable
```
Set-CMUpdateGroupDeployment [-Enable] -Deployment <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

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

### -Deployment
```yaml
Type: IResultObject
Parameter Sets: ByDeploymentSummaryValueDisable, ByDeploymentSummaryValueEnable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeploymentName
```yaml
Type: String
Parameter Sets: ByNameDisable, ByNameEnable
Aliases: Name, UpdateGroupDeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
```yaml
Type: SwitchParameter
Parameter Sets: ByNameDisable, ByIdDisable, ByValueDisable, ByDeploymentSummaryValueDisable
Aliases:

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

### -Enable
```yaml
Type: SwitchParameter
Parameter Sets: ByValueEnable, ByNameEnable, ByIdEnable, ByDeploymentSummaryValueEnable
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

### -UpdateGroupDeployment
```yaml
Type: IResultObject
Parameter Sets: ByValueEnable, ByValueDisable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -UpdateGroupDeploymentId
```yaml
Type: Int32
Parameter Sets: ByIdDisable, ByIdEnable
Aliases: Id

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
