---
description: Enables Configuration Manager deployment rules for automatic software updates.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Enable-CMSoftwareUpdateAutoDeploymentRule
---

# Enable-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Enables Configuration Manager deployment rules for automatic software updates.

## SYNTAX

### SearchByIdMandatory (Default)
```
Enable-CMSoftwareUpdateAutoDeploymentRule -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Enable-CMSoftwareUpdateAutoDeploymentRule -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Enable-CMSoftwareUpdateAutoDeploymentRule -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-CMSoftwareUpdateAutoDeploymentRule** cmdlet enables specified Configuration Manager deployment rules for automatic software updates.
While a rule is disabled, it does not run in accordance with its schedule and you cannot run it manually.

Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, Configuration Manager adds updates that qualify for the rule to a software update group.
The Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

You can specify rules to enable by ID or by name, or specify a rule object by using the [Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.
You can use the [Disable-CMSoftwareUpdateAutoDeploymentRule](Disable-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet to disable a rule.
To remove a rule permanently, use the [Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Enable a deployment rule by name
```
PS XYZ:\>Enable-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
```

This command enables a rule named Weekly Driver Updates.

### Example 2: Enable a deployment rule by ID
```
PS XYZ:\>Enable-CMSoftwareUpdateAutoDeploymentRule -Id "16777217"
```

This command enables a deployment rule that has the ID 16777217.

### Example 3: Enable a deployment rule by using a variable
```
PS XYZ:\> $CMSUADR = Get-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
PS XYZ:\> Enable-CMSoftwareUpdateAutoDeploymentRule -InputObject $CMSUADR
```

The first command gets a deployment rule that has the specified name, and then stores it in the $CMSUADR variable.

The second command enables the rule stored in the variable.

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

### -Id
Specifies an array of IDs for rules for automatic deployment of software updates.
This value is the **AutoDeploymentID** property of the deployment rule object.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: Named
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
Position: Named
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

[Disable-CMSoftwareUpdateAutoDeploymentRule](Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](Invoke-CMSoftwareUpdateAutoDeploymentRule.md)

[New-CMSoftwareUpdateAutoDeploymentRule](New-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md)

[Set-CMSoftwareUpdateAutoDeploymentRule](Set-CMSoftwareUpdateAutoDeploymentRule.md)


