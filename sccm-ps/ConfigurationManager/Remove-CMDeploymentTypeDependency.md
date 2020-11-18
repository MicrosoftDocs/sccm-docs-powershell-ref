---
description: Removes a deployment type dependency from Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/02/2019
schema: 2.0.0
title: Remove-CMDeploymentTypeDependency
---

# Remove-CMDeploymentTypeDependency

## SYNOPSIS

Removes a deployment type dependency from Configuration Manager deployment type dependency group.

## SYNTAX

```
Remove-CMDeploymentTypeDependency -DeploymentTypeDependency <IResultObject[]> [-Force]
 -InputObject <DeploymentTypeDependencyGroup> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Remove-CMDeploymentTypeDependency** cmdlet removes a deployment type dependency from a deployment type dependency group. If removing a dependency causes the group to have no more dependencies, the group will be removed. Required input is a deployment type object from [Get-CMDeploymentType](./Get-CMDeploymentType.md) or [Get-CMDeploymentTypeDependency](./Get-CMDeploymentTypeDependency.md) and a dependency group from [Get-CMDeploymentTypeDependencyGroup](./Get-CMDeploymentTypeDependencyGroup.md).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> $dpGroup = Get-CMDeploymentType -ApplicationName MyApp | Get-CMDeploymentTypeDependencyGroup -GroupName MyGroup
PS XYZ:\> $dpDeps = Get-CMDeploymentTypeDependency -Group $dpGroup
PS XYZ:\> Remove-CMDeploymentTypeDependency -Group $dpGroup -DeploymentTypeDependency $dpDeps[1] -Force
```

This command removes a deployment type dependency.

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

### -DeploymentTypeDependency

Specifies a deployment type object.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DeploymentTypeDependencies

Required: True
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

### -InputObject

Specifies a deployment type dependency group object.

```yaml
Type: DeploymentTypeDependencyGroup
Parameter Sets: (All)
Aliases: Group

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.ConfigurationManagement.Cmdlets.AppMan.Commands.DeploymentTypeDependencyGroup

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMDeploymentTypeDependency](./Add-CMDeploymentTypeDependency.md)

[Get-CMDeploymentTypeDependency](./Get-CMDeploymentTypeDependency.md)

[Set-CMDeploymentTypeDependency](./Set-CMDeploymentTypeDependency.md)
