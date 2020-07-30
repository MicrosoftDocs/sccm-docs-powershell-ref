---
description: Sets a deployment type dependency group in Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2018
schema: 2.0.0
title: Set-CMDeploymentTypeDependencyGroup
---

# Set-CMDeploymentTypeDependencyGroup

## SYNOPSIS

Sets a deployment type dependency group in Configuration Manager.

## SYNTAX

```
Set-CMDeploymentTypeDependencyGroup -InputObject <DeploymentTypeDependencyGroup> -NewName <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMDeploymentTypeDependencyGroup** cmdlet sets a deployment type dependency group in the Microsoft System Center Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\>  Get-CMDeploymentType -ApplicationName MyApp | Get-CMDeploymentTypeDependencyGroup -GroupName MyGroup | Set-CMDeploymentTypeDependencyGroup -NewName MyNewGroup
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

Specifies a deployment type dependency group.

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

### -NewName

Specifies a new dependency group name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: GroupName, NewGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.Cmdlets.AppMan.Commands.DeploymentTypeDependencyGroup

## OUTPUTS

### IResultObject#SMS_Application

## NOTES

## RELATED LINKS

[New-CMDeploymentTypeDependencyGroup](./New-CMDeploymentTypeDependencyGroup.md)

[Get-CMDeploymentTypeDependencyGroup](./Get-CMDeploymentTypeDependencyGroup.md)

[Remove-CMDeploymentTypeDependencyGroup](./Remove-CMDeploymentTypeDependencyGroup.md)
