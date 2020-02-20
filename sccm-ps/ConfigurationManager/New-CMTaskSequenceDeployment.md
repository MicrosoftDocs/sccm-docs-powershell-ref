---
author: mumian
description: Creates a task sequence deployment in Configuration Manager.
external help file: AdminUI.PS.Deployments.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: jgao
ms.date: 12/03/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
schema: 2.0.0
title: New-CMTaskSequenceDeployment
titleSuffix: Configuration Manager
---

# New-CMTaskSequenceDeployment

## SYNOPSIS

Creates a task sequence deployment in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
New-CMTaskSequenceDeployment [-InputObject] <IResultObject> [-DeadlineDateTime <DateTime>]
 [-DeployPurpose <DeployPurposeType>] [-Availability <MakeAvailableToType>]
 [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-ScheduleEvent <ScheduleEventType[]>] [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-InternetOption <Boolean>] [-PercentSuccess <Int32>] [-AlertDateTime <DateTime>]
 [-PercentFailure <Int32>] [-DeploymentOption <DeploymentOptionType>] [-AllowSharedContent <Boolean>]
 [-AllowFallback <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-UseMeteredNetwork <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
New-CMTaskSequenceDeployment [-DeadlineDateTime <DateTime>] [-TaskSequencePackageId] <String>
 [-DeployPurpose <DeployPurposeType>] [-Availability <MakeAvailableToType>]
 [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-ScheduleEvent <ScheduleEventType[]>] [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-InternetOption <Boolean>] [-PercentSuccess <Int32>] [-AlertDateTime <DateTime>]
 [-PercentFailure <Int32>] [-DeploymentOption <DeploymentOptionType>] [-AllowSharedContent <Boolean>]
 [-AllowFallback <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-UseMeteredNetwork <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMTaskSequenceDeployment** cmdlet creates a task sequence deployment.
A task sequence deployment assigns a task sequence to a collection of computers.

## EXAMPLES

## PARAMETERS

### -AlertDateTime

Specifies an alert date time.

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

### -AllowFallback

Indicates whether to allow clients to use a fallback source location for content.

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

### -AllowSharedContent

Indicates whether shared content is allowed.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowUseRemoteDistributionPoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Availability

Specifies availability.

```yaml
Type: MakeAvailableToType
Parameter Sets: (All)
Aliases: MakeAvailableTo
Accepted values: Clients, ClientsMediaAndPxe, MediaAndPxe, MediaAndPxeHidden

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableDateTime

Specifies an available date time.

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

### -Collection

Specifies a collection.

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

Specifies the ID of a collection.

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

Specifies a name of a collection designated to receive a task sequence deployment.
A collection is a group of client computers.

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

### -Comment

Specifies a comment for the task sequence deployment.

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

### -DeadlineDateTime

Specifies a deadline date time.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: DeploymentExpireDateTime

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeployPurpose

Specifies a deployment purpose.

```yaml
Type: DeployPurposeType
Parameter Sets: (All)
Aliases:
Accepted values: Available, Required

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentOption

Specifies if clients download all content before starting the task sequence, or download content as needed by the running task sequence.
By default, clients download content as needed.

```yaml
Type: DeploymentOptionType
Parameter Sets: (All)
Aliases:
Accepted values: DownloadContentLocallyWhenNeededByRunningTaskSequence, DownloadAllContentLocallyBeforeStartingTaskSequence, RunFromDistributionPoint

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

### -DistributeCollectionName

Specifies the name of a distribute collection.

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

### -DistributeContent

Specifies distribute content.

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

### -DistributionPointGroupName

Specifies the name of a distribution point group name.

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

### -DistributionPointName

Specifies the name of a distribution name.

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

Specifies a task sequence deployment object.
To obtain a task sequence object, use the [Get-CMTaskSequenceDeployment](Get-CMTaskSequenceDeployment.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: TaskSequence

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InternetOption

Indicates whether the task sequence runs on clients connecting over the Internet.

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

### -PercentFailure

Specifies a threshold percentage for failed task sequence deployment.

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

### -PercentSuccess

Specifies a threshold percentage for successful task sequence deployment.

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

### -PersistOnWriteFilterDevice

Indicates whether to install a task sequence on the temporary overlay and commit changes later, or commit the changes at an installation deadline or a maintenance window.

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

### -RerunBehavior

Specifies that a task sequence will be rerun on a computer if it has previously been run before the scheduled mandatory time.
By default, the task sequence is always rerun.

```yaml
Type: RerunBehaviorType
Parameter Sets: (All)
Aliases:
Accepted values: NeverRerunDeployedProgram, AlwaysRerunProgram, RerunIfFailedPreviousAttempt, RerunIfSucceededOnPreviousAttempt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunFromSoftwareCenter

Indicate whether to run from software center.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowUsersRunIndependently

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule

Specifies an array of **CMSchedule** objects.
A **CMSchedule** object defines the mandatory assignment schedule for a deployment.
To create a **CMSchedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScheduleEvent

Specifies an array of events that determine when the task sequence deployment runs.
The acceptable values for this parameter are:

- AsSoonAsPossible
- LogOff
- LogOn

```yaml
Type: ScheduleEventType[]
Parameter Sets: (All)
Aliases:
Accepted values: AsSoonAsPossible, LogOn, LogOff

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendWakeupPacket

Indicates whether to send a wake-up packet to computers before the deployment begins.
If this value is $True, Configuration Manager wakes a computer from sleep.
If this value is $False, it does not wake computers from sleep.
For computers to wake, you must first configure Wake On LAN.

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

### -ShowTaskSequenceProgress

Indicates whether to show a process dialog for a task sequence.

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

### -SoftwareInstallation

Indicates whether to allow the application to install, even if the installation occurs outside of a maintenance window.

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

### -SystemRestart

Indicates whether to allow an advertised program to restart the system, even if the restart occurs outside of a maintenance window.

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

### -TaskSequencePackageId

Specifies the ID of a task sequence package.

```yaml
Type: String
Parameter Sets: SearchPackageByIdMandatory
Aliases: PackageId, TaskSequenceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseMeteredNetwork

Indicates whether to allow clients on a metered Internet connection to download content after the installation deadline, which might incur additional costs.

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

### -UseUtcForAvailableSchedule

Indicates whether client computers use UTC time to determine the availability of a program.
UTC time makes the task sequence available at the same time for all computers.

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

### -UseUtcForExpireSchedule

Indicates whether client computers use UTC time to determine the expiration of a program.
UTC time makes the task sequence available at the same time for all computers.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_Advertisement

## NOTES

## RELATED LINKS

[Get-CMTaskSequenceDeployment](./Get-CMTaskSequenceDeployment.md)
[Set-CMTaskSequenceDeployment](./Set-CMTaskSequenceDeployment.md)
[Start-CMTaskSequenceDeployment](./Start-CMTaskSequenceDeployment.md)
[Remove-CMTaskSequenceDeployment](./Remove-CMTaskSequenceDeployment.md)
