---
author: aczechowski
description: Changes settings for a Configuration Manager baseline deployment.
external help file: AdminUI.PS.Deployments.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMBaselineDeployment
titleSuffix: Configuration Manager
---

# Set-CMBaselineDeployment

## SYNOPSIS
Changes settings for a Configuration Manager baseline deployment.

## SYNTAX

### SetBaselineDeploymentByValueMandatory (Default)
```
Set-CMBaselineDeployment -InputObject <IResultObject> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>] [-PassThru]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetBaselineDeploymentByNameMandatory
```
Set-CMBaselineDeployment -BaselineName <String> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>] [-PassThru]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetBaselineDeploymentByIdMandatory
```
Set-CMBaselineDeployment -BaselineId <String> [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>]
 [-GenerateAlert <Boolean>] [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>]
 [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>] [-PassThru] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMBaselineDeployment** cmdlet changes settings for a Microsoft System Center Configuration Manager baseline configuration deployment.
A baseline defines the configuration of a product or system established at a specific time.
Baselines contain a defined set of required configurations and associated rules.
System Center Configuration Manager assigns baselines to computer in collections, together with a compliance evaluation schedule.

Use the baseline and the name of a collection to specify a deployment to modify.
You can specify a baseline by its name or ID, or use the **Get-CMBaseline** cmdlet to get a baseline object.

You can use the **Start-CMBaselineDeployment** cmdlet to begin a deployment.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Change whether a deployment generates alerts
```
PS XYZ:\> Set-CMBaselineDeployment -BaselineName "Baseline 2012" -CollectionName "All Computers" -GenerateAlert $False
```

This command changes a deployment for the baseline named Baseline 2012 for a collection named All Computers.
This command sets the *GenerateAlert* parameter to $False.

### Example 2: Change deployment settings
```
PS XYZ:\> Set-CMBaselineDeployment -BaselineName "Baseline A3" -CollectionName "TSQA Computers" -GenerateAlert $True -MonitoredByScom $True -ParameterValue 60 -PostponeDate 2013/02/12 -PostponeTime 12:34
```

This command changes a deployment for the baseline named Baseline A3 for a collection named TSQA Computers.
The command specifies values for generation of alerts and Operations Manager monitoring.
It also includes as a parameter value and postpone date and time.

## PARAMETERS

### -BaselineId
Specifies the ID of a baseline.

```yaml
Type: String
Parameter Sets: SetBaselineDeploymentByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BaselineName
Specifies the name of a baseline.

```yaml
Type: String
Parameter Sets: SetBaselineDeploymentByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
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

### -CollectionName
Specifies the name of a collection.
The deployment applies to this collection.

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

### -EnableEnforcement
Specifies whether to enable enforcement for the baseline.
During enforcement, a client reports compliance information about the configurations in a baseline.

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

### -GenerateAlert
Specifies whether Configuration Manager generates alerts during the deployment.

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

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: SetBaselineDeploymentByValueMandatory
Aliases: Baseline, DeploymentSummary, Assignment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MonitoredByScom
Specifies whether to apply System Center 2016 - Operations Manager monitoring criteria during the deployment.

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

### -OverrideServiceWindow
Specifies whether to override service windows while deploying policies.
Service windows are periods of time allocated for maintenance.

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

### -ParameterValue
Specifies an integer value.
This is the parameter value.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
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

### -PostponeDateTime
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a **CMSchedule** object.
The schedule specifies when the maintenance window occurs.
To create a **CMSchedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Start-CMBaselineDeployment](Start-CMBaselineDeployment.md)

[Get-CMBaseline](Get-CMBaseline.md)
