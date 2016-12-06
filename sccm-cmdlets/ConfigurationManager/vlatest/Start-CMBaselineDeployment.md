---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834199
schema: 2.0.0
ms.assetid: 4EA07297-564A-4DA0-957D-5ADE49683D74
---

# Start-CMBaselineDeployment

## SYNOPSIS
Starts deployment of a Configuration Manager baseline configuration to a collection of computers.

## SYNTAX

### SearchByValueMandatory (Default)
```
Start-CMBaselineDeployment [-InputObject] <IResultObject> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Start-CMBaselineDeployment [-Id] <Int32> -CollectionName <String> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Start-CMBaselineDeployment [-Name] <String> -CollectionName <String> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMBaselineDeployment** cmdlet starts the deployment of a Microsoft System Center Configuration Manager baseline configuration to a collection of computers.

A baseline defines the configuration of a product or system established at a specific time.
Baselines contain a defined set of required configurations and associated rules.
System Center Configuration Manager assigns baselines to computer in collections, together with a compliance evaluation schedule.

## EXAMPLES

### Example 1: Start baseline deployment
```
PS C:\>Start-CMBaselineDeployment -CollectionName "All Users" -Name "Baseline22" -EnableEnforcement $True -GenerateAlert $True -MonitoredByScom $True -OverrideServiceWindow $True -ParameterValue 30
```

This command starts a baseline deployment named Baseline22 for the collection All Users.
The command enables enforcement, generates alerts, monitors the deployment using Operations Manager, and overrides defined service windows.
The command specifies a parameter value of 30.

## PARAMETERS

### -CollectionName
Specifies a name of a collection.
The deployment applies to this collection.

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
Indicates that wildcard handling is disabled.

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
Indicates whether to enable enforcement for the deployment.
During enforcement, a client reports compliance information about a deployment.

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
Indicates that wildcard handling is enabled.

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
Indicates whether Configuration Manager generates alerts during the deployment.

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
Specifies an array of IDs of baseline deployments.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a baseline deployment object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 
Required: True
Position: 0
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

### -Name
Specifies an array of names for baseline deployments.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideServiceWindow
Indicates whether to override service windows while deploying policies.
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

### -PostponeDate
Specifies a date, as a **DateTime** object.
To obtain a **DateTime** object, use the Get-Date cmdlet.
For more information, type `Get-Help Get-Date`.
This is the date for the deployment if postponed.

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

### -PostponeTime
Specifies a time, as a **DateTime** object.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.
This is the time for the deployment if postponed.

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
Specifies a schedule object.
This is the schedule for evaluating the baseline.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMBaselineDeployment](./Set-CMBaselineDeployment.md)


