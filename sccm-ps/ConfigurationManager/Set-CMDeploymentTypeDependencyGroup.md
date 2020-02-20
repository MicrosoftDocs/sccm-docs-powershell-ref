---
author: mumian
description: Sets a deployment type dependency group in Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: jgao
ms.date: 12/03/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
schema: 2.0.0
title: Set-CMDeploymentTypeDependencyGroup
titleSuffix: Configuration Manager
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

## EXAMPLES

### Example 1

```powershell
PS XYZ:\>  Get-CMDeploymentType -ApplicationName MyApp | Get-CMDeploymentTypeDependencyGroup -GroupName MyGroup | Set-CMDeploymentTypeDependencyGroup -NewName MyNewGroup
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

### IResultObject#SMS_Application

## NOTES

## RELATED LINKS

[New-CMDeploymentTypeDependencyGroup](./New-CMDeploymentTypeDependencyGroup.md)

[Get-CMDeploymentTypeDependencyGroup](./Get-CMDeploymentTypeDependencyGroup.md)

[Remove-CMDeploymentTypeDependencyGroup](./Remove-CMDeploymentTypeDependencyGroup.md)
