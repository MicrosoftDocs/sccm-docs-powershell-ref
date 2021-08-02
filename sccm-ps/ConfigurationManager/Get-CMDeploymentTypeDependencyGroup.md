---
description: Gets a deployment type dependency group from Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2018
schema: 2.0.0
title: Get-CMDeploymentTypeDependencyGroup
---

# Get-CMDeploymentTypeDependencyGroup

## SYNOPSIS

Gets a deployment type dependency group from Configuration Manager.

## SYNTAX

```
Get-CMDeploymentTypeDependencyGroup [-GroupId <String>] [-GroupName <String>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMDeploymentTypeDependencyGroup** cmdlet gets a deployment type dependency group from the Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\>  Get-CMDeploymentType -ApplicationName MyApp | Get-CMDeploymentTypeDependencyGroup
```

This command returns the dependency groups of a deployment type.

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

### -GroupId
{{ Fill GroupId Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GroupName

Specifies a dependency group name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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
Aliases: DeploymentType

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

### DeploymentTypeDependencyGroup[]
### DeploymentTypeDependency
## NOTES

## RELATED LINKS

[New-CMDeploymentTypeDependencyGroup](./New-CMDeploymentTypeDependencyGroup.md)

[Set-CMDeploymentTypeDependencyGroup](./Set-CMDeploymentTypeDependencyGroup.md)

[Remove-CMDeploymentTypeDependencyGroup](./Remove-CMDeploymentTypeDependencyGroup.md)
