<<<<<<< HEAD
---
title: New-CMBaselineDeployment
titleSuffix: Configuration Manager
description: Creates a baseline deployment.
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: 
schema: 2.0.0
>>>>>>> master
---

# New-CMBaselineDeployment

## SYNOPSIS
Creates a baseline deployment.

## SYNTAX

### SearchByValueMandatory (Default)
```
New-CMBaselineDeployment [-InputObject] <IResultObject> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMBaselineDeployment [-Id] <Int32> [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>]
 [-GenerateAlert <Boolean>] [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>]
 [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMBaselineDeployment [-Name] <String> [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>]
 [-GenerateAlert <Boolean>] [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>]
 [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1 - Deploy Baseline to several Collections that Start with the Name "Collection_Name"
```
PS XYZ:\>  $BaselineName = Get-CMBaseline -Name 'ConfigMgr Baseline'
PS XYZ:\>  $DeployToCollections = Get-CMCollection -Name 'Collection_Name*' | Sort-Object -Property "Name"
PS XYZ:\>  $BaselineSchedule = New-CMSchedule -DurationInterval Days -DurationCount 0 -RecurInterval Days -RecurCount 1
PS XYZ:\>  foreach ($Collection in $DeployToCollection)
             {
             New-CMBaselineDeployment -InputObject $BaselineName -CollectionID $Collection.CollectionId -Schedule $BaselineSchedule
             Write-Output "Created Deployment for $($BaselineName.LocalizedDisplayName) on $($Collection.Name)"
             }
             
```
This Example Grabs the Baseline we want to deploy and places it into the variable $BaselineName (InputObject) using [Get-CMBaseline](https://docs.microsoft.com/en-us/powershell/module/configurationmanager/get-cmbaseline), we then grab a list of all the collections we wish to deploy it to ($DeployToCollections) using [Get-CMCollection](https://docs.microsoft.com/en-us/powershell/module/configurationmanager/get-cmcollection).  We then need to create a schedule for the deployment using [New-CMSchedule](https://docs.microsoft.com/en-us/powershell/module/configurationmanager/new-cmschedule). Once we have all of the required information, we can deploy the baseline to those collections using New-CMBaselineDeployment.

### Example 2 - Deploy Baseline to one Collection
```
PS XYZ:\>  $BaselineSchedule = New-CMSchedule -DurationInterval Days -DurationCount 0 -RecurInterval Days -RecurCount 1
PS XYZ:\>  New-CMBaselineDeployment -Name "MY_Baseline" -CollectionID "PS1000023" -Schedule $BaselineSchedule
```

This first creates a simple schedule, then deployes the Baseline "MyName" to Collection ID: PS1000023 using that schedule.

## PARAMETERS

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

### -EnableEnforcement
 

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

### -Id
 

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID, BaselineId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
 

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Baseline

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MonitoredByScom
 

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

### -Name
 

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName, BaselineName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideServiceWindow
 

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

