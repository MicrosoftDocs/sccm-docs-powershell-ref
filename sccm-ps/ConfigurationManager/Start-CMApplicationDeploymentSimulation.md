---
description: Starts an application deployment simulation in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Start-CMApplicationDeploymentSimulation
---

# Start-CMApplicationDeploymentSimulation

## SYNOPSIS
(Deprecated) Starts an application deployment simulation in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Start-CMApplicationDeploymentSimulation -CollectionName <String> [-DeploymentAction <DeployActionType>]
 -InputObject <IResultObject> [-PreDeploy <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Start-CMApplicationDeploymentSimulation -CollectionName <String> [-DeploymentAction <DeployActionType>]
 -Id <Int32> [-PreDeploy <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Start-CMApplicationDeploymentSimulation -CollectionName <String> [-DeploymentAction <DeployActionType>]
 -Name <String> [-PreDeploy <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **Start-CMApplicationDeploymentSimulation** cmdlet starts an application deployment.
Use simulated deployment to test an application deployment without installing an application.

> [!IMPORTANT]
> Starting in version 2107, this cmdlet is deprecated and may be removed in a future release. Instead use the [New-CMApplicationDeployment](New-CMApplicationDeployment.md) cmdlet with the **Simulation** parameter.

## EXAMPLES

### Example 1: Start an application deployment simulation
```
PS XYZ:\> Start-CMApplicationDeploymentSimulation -CollectionName "All Mobile Devices" -Name "WIN8_UPDATE2" -DeployAction Install
```

This command starts a deployment simulation of the installation of the application named WIN8_UPDATE2 for the target collection named All Mobile Devices.

## PARAMETERS

### -CollectionName
Specifies a name for the target collection.

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

### -DeploymentAction
```yaml
Type: DeployActionType
Parameter Sets: (All)
Aliases: DeployAction
Accepted values: Install, Uninstall

Required: False
Position: Named
Default value: None
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
Specifies an array of IDs.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an application deployment object.

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
Specifies an array of names.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreDeploy
Indicates whether to copy software to a device before installation.

```yaml
Type: Boolean
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

[Set-CMApplicationDeployment](Set-CMApplicationDeployment.md)

[Start-CMApplicationDeployment](Start-CMApplicationDeployment.md)
