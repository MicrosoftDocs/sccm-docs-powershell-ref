---
description: Gets a deployment type dependency.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/02/2019
schema: 2.0.0
title: Get-CMDeploymentTypeDependency
---

# Get-CMDeploymentTypeDependency

## SYNOPSIS

Gets a deployment type from a dependency group.

## SYNTAX

```
Get-CMDeploymentTypeDependency -InputObject <DeploymentTypeDependencyGroup> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMDeploymentTypeDependency** cmdlet gets existing dependent deployment types from a dependency group. Required input is a dependency group object from [Get-CMDeploymentTypeDependencyGroup](./Get-CMDeploymentTypeDependencyGroup.md).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> Get-CMDeploymentType -ApplicationName MyApp | Get-CMDeploymentTypeDependencyGroup -GroupName MyGroup | Get-CMDeploymentTypeDependency
```

This command gets a deployment type from a dependency group.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.AppMan.DeploymentTypeDependencyGroup
## OUTPUTS

### IResultObject[]#SMS_DeploymentType
### IResultObject#SMS_DeploymentType
## NOTES

## RELATED LINKS

[Add-CMDeploymentTypeDependency](./Add-CMDeploymentTypeDependency.md)

[Set-CMDeploymentTypeDependency](./Set-CMDeploymentTypeDependency.md)

[Remove-CMDeploymentTypeDependency](./Remove-CMDeploymentTypeDependency.md)
