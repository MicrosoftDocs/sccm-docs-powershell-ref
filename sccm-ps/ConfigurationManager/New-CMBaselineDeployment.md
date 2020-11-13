---
description: Create a baseline deployment
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/24/2020
schema: 2.0.0
title: New-CMBaselineDeployment
---

# New-CMBaselineDeployment

## SYNOPSIS

Create a baseline deployment.

## SYNTAX

### SearchByValueMandatory (Default)
```
New-CMBaselineDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-InputObject] <IResultObject> [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMBaselineDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>] [-Id] <Int32>
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMBaselineDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>] [-MonitoredByScom <Boolean>]
 [-Name] <String> [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>]
 [-Schedule <IResultObject>] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Deploy a configuration baseline. Use the [Get-CMBaseline](Get-CMBaseline.md) cmdlet to get a baseline.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Deploy a baseline to collections with the same named prefix

This example uses [Get-CMBaseline](Get-CMBaseline.md) to get the configuration baseline and store it into the variable **$BaselineName**. It then uses [Get-CMCollection](Get-CMCollection.md) to get a list of all collections whose name starts with "Collection_Name" and stores them to the variable **$DeployToCollections**.  Next, it creates a schedule for the deployment with the [New-CMSchedule](New-CMSchedule.md) cmdlet. Once all of the required information is stored, the example loops through each collection and deploys the baseline using **New-CMBaselineDeployment**.

```powershell
$BaselineName = Get-CMBaseline -Name 'ConfigMgr Baseline'
$DeployToCollections = Get-CMCollection -Name 'Collection_Name*' | Sort-Object -Property "Name"
$BaselineSchedule = New-CMSchedule -DurationInterval Days -DurationCount 0 -RecurInterval Days -RecurCount 1

foreach ($Collection in $DeployToCollection)
             {
             New-CMBaselineDeployment -InputObject $BaselineName -CollectionID $Collection.CollectionId -Schedule $BaselineSchedule
             Write-Output "Created Deployment for $($BaselineName.LocalizedDisplayName) on $($Collection.Name)"
             }
```

### Example 2: Deploy a baseline to one collection

First, this example creates a simple schedule. It then deploys the baseline **MY_Baseline** to the collection with ID **PS1000023**.

```powershell
$BaselineSchedule = New-CMSchedule -DurationInterval Days -DurationCount 0 -RecurInterval Days -RecurCount 1
New-CMBaselineDeployment -Name "MY_Baseline" -CollectionID "PS1000023" -Schedule $BaselineSchedule
```

## PARAMETERS

### -Collection

Specify a collection object as the target of the baseline deployment.

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

Specify the ID of the collection as the target of the deployment.

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

Specify the name of the collection as the target of the deployment.

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

### -EnableEnforcement

If `$true`, remediate noncompliant rules when supported.

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

### -GenerateAlert

If `$true`, generate an alert.

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

Specify the ID of the configuration baseline to deploy.

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

Specify a configuration baseline object to deploy. Use the [Get-CMBaseline](Get-CMBaseline.md) cmdlet to get a baseline.

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

If `$true`, generate a System Center Operations Manager alert.

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

Specify the name of the configuration baseline to deploy.

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

If `$true`, allow the client to remediate this baseline outside of maintenance windows.

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

If you use the **-GenerateAlert** parameter, specify an integer value as a percentage (0-100). When compliance of this configuration baseline is below this value, the site generates an alert.

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

This parameter corresponds to the **Date and time** property of the configuration baseline when you use the **-GenerateAlert** parameter.

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

Specify a schedule object for when the client evaluates this configuration baseline. Use the [New-CMSchedule](New-CMSchedule.md) cmdlet to create a schedule.

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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMBaseline](Get-CMBaseline.md)

[Get-CMCollection](Get-CMCollection.md)

[New-CMSchedule](New-CMSchedule.md)
