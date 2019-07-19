<<<<<<< HEAD
---
title: Remove-CMSoftwareUpdateAutoDeploymentRule
titleSuffix: Configuration Manager
description: Removes Configuration Manager deployment rules for automatic software updates.
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
ms.assetid: EE878F33-0D30-45F6-A72B-43BEFEFE4E07
online version: https://go.microsoft.com/fwlink/?linkid=834217
schema: 2.0.0
>>>>>>> master
---

# Remove-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Removes Configuration Manager deployment rules for automatic software updates.

## SYNTAX

### SearchByIdMandatory (Default)
```
Remove-CMSoftwareUpdateAutoDeploymentRule [-Id] <Int32> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSoftwareUpdateAutoDeploymentRule [-Name] <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMSoftwareUpdateAutoDeploymentRule [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSoftwareUpdateAutoDeploymentRule** cmdlet removes specified Microsoft System Center Configuration Manager deployment rules for automatic software updates.

System Center Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, System Center Configuration Manager adds updates that qualify for the rule to a software update group.
The System Center Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

You can specify rules to remove by ID or by name, or specify a rule object by using the [Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.
This cmdlet deletes rules permanently.
You can use the [Disable-CMSoftwareUpdateAutoDeploymentRule](Disable-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet to suspend a rule.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove a deployment rule by name
```
PS XYZ:\> Remove-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
Remove
Are you sure you wish to remove SoftwareUpdateAutoDeploymentRule: Name="Weekly Driver Updates"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

This command removes a rule named Weekly Driver Updates.
Because the command does not include the *Force* parameter, the cmdlet prompts you before it deletes the rule.

### Example 2: Remove a deployment rule by ID
```
PS XYZ:\> Remove-CMSoftwareUpdateAutoDeploymentRule -Id "16777217" -Force
```

This command disables a deployment rule that has the ID 16777217.
This command includes the *Force* parameter, so the cmdlet does not prompt you before it removes the rule.

### Example 3: Remove a deployment rule by using a variable
```
PS XYZ:\> $CMSUADR = Get-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
PS XYZ:\> Remove-CMSoftwareUpdateAutoDeploymentRule -InputObject $CMSUADR -Force
```

The first command gets a deployment rule that has the specified name, and then stores it in the $CMSUADR variable.

The second command removes the rule stored in the variable.

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

### -Id
Specifies an array of IDs for rules for automatic deployment of software updates.
This value is the **AutoDeploymentID** property of the deployment rule object.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software update automatic deployment rule object.
To obtain a deployment rule object, use **Get-CMSoftwareUpdateAutoDeploymentRule**.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a rule for automatic deployment of software updates.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: True
Position: 0
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

[Disable-CMSoftwareUpdateAutoDeploymentRule](Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Enable-CMSoftwareUpdateAutoDeploymentRule](Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](Invoke-CMSoftwareUpdateAutoDeploymentRule.md)


