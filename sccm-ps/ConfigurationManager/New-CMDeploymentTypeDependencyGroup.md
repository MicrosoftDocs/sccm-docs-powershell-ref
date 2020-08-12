---
description: Creates a deployment type dependency group in Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2018
schema: 2.0.0
title: New-CMDeploymentTypeDependencyGroup
---

# New-CMDeploymentTypeDependencyGroup

## SYNOPSIS

Creates a deployment type dependency group in Configuration Manager.

## SYNTAX

```
New-CMDeploymentTypeDependencyGroup -GroupName <String> -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMDeploymentTypeDependencyGroup** cmdlet creates a deployment type dependency group in the Configuration Manager.
Must be added to an existing deployment type by using [Add-CMDeploymentTypeDependency](./Add-CMDeploymentTypeDependency.md).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\>  Get-CMDeploymentType -ApplicationName MyApp | New-CMDeploymentTypeDependencyGroup -GroupName MyGroup
```

This command creates a new dependency group call MyGroup for the deployment type MyApp.

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

### -GroupName

Specifies a group name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies a deployment type object.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: ParentDeploymentType, DependingDeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.AppMan.Commands.DeploymentTypeDependencyGroup

## NOTES

## RELATED LINKS

[Get-CMDeploymentTypeDependencyGroup](./Get-CMDeploymentTypeDependencyGroup.md)

[Set-CMDeploymentTypeDependencyGroup](./Set-CMDeploymentTypeDependencyGroup.md)

[Remove-CMDeploymentTypeDependencyGroup](./Remove-CMDeploymentTypeDependencyGroup.md)
