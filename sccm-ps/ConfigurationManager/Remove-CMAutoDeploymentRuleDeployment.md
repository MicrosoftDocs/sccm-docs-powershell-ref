---
description: Removes a deployment from an auto deployment rule.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMAutoDeploymentRuleDeployment
---

# Remove-CMAutoDeploymentRuleDeployment

## SYNOPSIS
Removes a deployment from an auto deployment rule.

## SYNTAX

```
Remove-CMAutoDeploymentRuleDeployment [-Force] [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAutoDeploymentRuleDeployment** cmdlet removes a deployment from an auto deployment rule.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a deployment
```
PS XYZ:\> $Deployments = Get-CMAutoDeploymentRuleDeployment -Name "TestRule01"
PS XYZ:\> Remove-CMAutoDeploymentRuleDeployment -InputObject $Deployments[0]
```

The first command gets the deployment objects associated with the automatic deployment rule named TestRule01 and stores the objects in the $Deployments variable.

The second command removes the first deployment object stored in $Deployments.

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

### -InputObject
Specifies an automatic deployment rule deployment object.
To obtain a deployment object, use the [Get-CMAutoDeploymentRuleDeployment](Get-CMAutoDeploymentRuleDeployment.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: AutoDeploymentRuleDeployment

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

###  

## NOTES

## RELATED LINKS

[Get-CMAutoDeploymentRuleDeployment](Get-CMAutoDeploymentRuleDeployment.md)

[New-CMAutoDeploymentRuleDeployment](New-CMAutoDeploymentRuleDeployment.md)

[Set-CMAutoDeploymentRuleDeployment](Set-CMAutoDeploymentRuleDeployment.md)
