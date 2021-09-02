---
description: Configure a task sequence deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: Set-CMTaskSequenceDeployment
---

# Set-CMTaskSequenceDeployment

## SYNOPSIS

Configure a task sequence deployment.

## SYNTAX

### SetTaskSequenceDeploymentByValueMandatory (Default)
```
Set-CMTaskSequenceDeployment [-AlertDateTime <DateTime>] [-AllowFallback <Boolean>]
 [-AllowSharedContent <Boolean>] [-AllowUsersRunIndependently <Boolean>] [-Comment <String>]
 [-CreateAlertOnFailure <Boolean>] [-CreateAlertOnSuccess <Boolean>] [-DeploymentAvailableDateTime <DateTime>]
 [-DeploymentExpireDateTime <DateTime>] [-DeploymentOption <DeploymentOptionType>] -InputObject <IResultObject>
 [-InternetOption <Boolean>] [-MakeAvailableTo <MakeAvailableToType>] [-PercentFailure <Int32>]
 [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>] [-RerunBehavior <RerunBehaviorType>]
 [-ClearSchedule] [-RemoveSchedule <IResultObject[]>] [-AddSchedule <IResultObject[]>]
 [-Schedule <IResultObject[]>] [-ClearScheduleEvent] [-RemoveScheduleEvent <ScheduleEventType[]>]
 [-AddScheduleEvent <ScheduleEventType[]>] [-ScheduleEvent <ScheduleEventType[]>] [-SendWakeupPacket <Boolean>]
 [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetTaskSequenceDeploymentByDeploymentIdMandatory
```
Set-CMTaskSequenceDeployment [-AlertDateTime <DateTime>] [-AllowFallback <Boolean>]
 [-AllowSharedContent <Boolean>] [-AllowUsersRunIndependently <Boolean>] [-Comment <String>]
 [-CreateAlertOnFailure <Boolean>] [-CreateAlertOnSuccess <Boolean>] [-DeploymentAvailableDateTime <DateTime>]
 [-DeploymentExpireDateTime <DateTime>] [-DeploymentOption <DeploymentOptionType>] [-InternetOption <Boolean>]
 [-MakeAvailableTo <MakeAvailableToType>] [-PercentFailure <Int32>] [-PercentSuccess <Int32>]
 [-PersistOnWriteFilterDevice <Boolean>] [-RerunBehavior <RerunBehaviorType>] [-ClearSchedule]
 [-RemoveSchedule <IResultObject[]>] [-AddSchedule <IResultObject[]>] [-Schedule <IResultObject[]>]
 [-ClearScheduleEvent] [-RemoveScheduleEvent <ScheduleEventType[]>] [-AddScheduleEvent <ScheduleEventType[]>]
 [-ScheduleEvent <ScheduleEventType[]>] [-SendWakeupPacket <Boolean>] [-ShowTaskSequenceProgress <Boolean>]
 [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>] -TaskSequenceDeploymentId <String>
 [-UseMeteredNetwork <Boolean>] [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetTaskSequenceDeploymentByNameMandatory
```
Set-CMTaskSequenceDeployment [-AlertDateTime <DateTime>] [-AllowFallback <Boolean>]
 [-AllowSharedContent <Boolean>] [-AllowUsersRunIndependently <Boolean>] [-Comment <String>]
 [-CreateAlertOnFailure <Boolean>] [-CreateAlertOnSuccess <Boolean>] [-DeploymentAvailableDateTime <DateTime>]
 [-DeploymentExpireDateTime <DateTime>] [-DeploymentOption <DeploymentOptionType>] [-InternetOption <Boolean>]
 [-MakeAvailableTo <MakeAvailableToType>] [-PercentFailure <Int32>] [-PercentSuccess <Int32>]
 [-PersistOnWriteFilterDevice <Boolean>] [-RerunBehavior <RerunBehaviorType>] [-ClearSchedule]
 [-RemoveSchedule <IResultObject[]>] [-AddSchedule <IResultObject[]>] [-Schedule <IResultObject[]>]
 [-ClearScheduleEvent] [-RemoveScheduleEvent <ScheduleEventType[]>] [-AddScheduleEvent <ScheduleEventType[]>]
 [-ScheduleEvent <ScheduleEventType[]>] [-SendWakeupPacket <Boolean>] [-ShowTaskSequenceProgress <Boolean>]
 [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>] -TaskSequenceName <String>
 [-UseMeteredNetwork <Boolean>] [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetTaskSequenceDeploymentByIdMandatory
```
Set-CMTaskSequenceDeployment [-AlertDateTime <DateTime>] [-AllowFallback <Boolean>]
 [-AllowSharedContent <Boolean>] [-AllowUsersRunIndependently <Boolean>] [-Comment <String>]
 [-CreateAlertOnFailure <Boolean>] [-CreateAlertOnSuccess <Boolean>] [-DeploymentAvailableDateTime <DateTime>]
 [-DeploymentExpireDateTime <DateTime>] [-DeploymentOption <DeploymentOptionType>] [-InternetOption <Boolean>]
 [-MakeAvailableTo <MakeAvailableToType>] [-PercentFailure <Int32>] [-PercentSuccess <Int32>]
 [-PersistOnWriteFilterDevice <Boolean>] [-RerunBehavior <RerunBehaviorType>] [-ClearSchedule]
 [-RemoveSchedule <IResultObject[]>] [-AddSchedule <IResultObject[]>] [-Schedule <IResultObject[]>]
 [-ClearScheduleEvent] [-RemoveScheduleEvent <ScheduleEventType[]>] [-AddScheduleEvent <ScheduleEventType[]>]
 [-ScheduleEvent <ScheduleEventType[]>] [-SendWakeupPacket <Boolean>] [-ShowTaskSequenceProgress <Boolean>]
 [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>] -TaskSequencePackageId <String>
 [-UseMeteredNetwork <Boolean>] [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMTaskSequenceDeployment** cmdlet configures a task sequence deployment. A task sequence deployment assigns a task sequence to a collection of computers.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Configure a deployment to show progress

This command configures the task sequence deployment by using the task sequence name and collection name. It sets the comment and enables the client to show task sequence progress.

```powershell
Set-CMTaskSequenceDeployment -TaskSequenceName "Task Sequence 1333" -CollectionName "All Systems" -Comment "Task sequence test" -ShowTaskSequenceProgress $True
```

### Example 2: Reconfigure a task sequence deployment

This command reconfigures most of the settings for a task sequence deployment.

```powershell
Set-CMTaskSequenceDeployment -TaskSequenceName "Task Sequence 1333" -CollectionName "All Desktop and Server Clients" -Comment "Task sequence test" -SendWakeupPacket $True -UseMeteredNetwork $True -DeploymentExpireDateTime $(Get-Date) -ScheduleEvent LogOff -RerunBehavior NeverRerunDeployedProgram -AllowUsersRunIndependently $True -ShowTaskSequenceProgress $False -SoftwareInstallation $True -SystemRestart $True -PersistOnWriteFilterDevice $False -InternetOption $True -DeploymentOption DownloadAllContentLocallyBeforeStartingTaskSequence -AllowFallback $True -AllowSharedContent $True
```

## PARAMETERS

### -AddSchedule

Specify a schedule token object to add to the deployment. To create a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -AddScheduleEvent

Specify one of the accepted schedule events to add to the deployment.

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

Indicates whether to allow shared content.

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

### -AllowUsersRunIndependently

Indicates whether to allow users to independently run the program, regardless of its assignment status.

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

### -ClearSchedule

Add this parameter to remove all schedules from the deployment.

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

### -ClearScheduleEvent

Add this parameter to remove all schedule events from the deployment.

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

### -Collection

Specifies a collection object as the target of the deployment.

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

Specifies the ID of a collection as the target of the deployment.

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

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Comment

Specifies a optional comment for the task sequence deployment to help describe it.

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

### -CreateAlertOnFailure

Indicates whether to create an alert on failure.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CreateAlertBaseOnPercentFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateAlertOnSuccess

Indicates whether to create an alert on success.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CreateAlertBaseOnPercentSuccess

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentAvailableDateTime

Specifies deployment available date time.

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

### -DeploymentExpireDateTime

Specifies deployment expire date time.

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

### -DeploymentOption

Specifies if clients download all content before starting the task sequence, or download content as needed by the running task sequence.

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

### -InputObject

Specifies a task sequence deployment object. To get a task sequence object, use the [Get-CMTaskSequenceDeployment](Get-CMTaskSequenceDeployment.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetTaskSequenceDeploymentByValueMandatory
Aliases: Deployment, DeploymentSummary, TaskSequence, Advertisement

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InternetOption

Indicates whether the task sequence runs on clients connecting over the internet.

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

### -MakeAvailableTo

Specifies whether to make this task sequence available to Configuration Manager clients, and whether to make it available when you deploy an OS by using boot media, prestaged media, or PXE.

```yaml
Type: MakeAvailableToType
Parameter Sets: (All)
Aliases:
Accepted values: Clients, ClientsMediaAndPxe, MediaAndPxe, MediaAndPxeHidden

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Returns the current working object. By default, this cmdlet doesn't generate any output.

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

Indicates whether to install a task sequence on the temporary overlay and commit changes later, or commit the changes at an installation deadline or a maintenance window. This setting applies to devices running an embedded edition of Windows with a write filter.

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

### -RemoveSchedule

Specify a schedule token object to remove from the deployment. To create a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -RemoveScheduleEvent

Specify one of the accepted schedule events to remove from the deployment.

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

### -RerunBehavior

Specifies whether the task sequence will rerun on a computer if it previously ran before the scheduled mandatory time. By default, the task sequence always reruns.

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

### -Schedule

Specifies an array of **CMSchedule** objects. A **CMSchedule** object defines the mandatory assignment schedule for a deployment. To create a **CMSchedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

Indicates whether to send a wake-up packet to computers before the deployment begins. If this value is `$True`, Configuration Manager wakes a computer from sleep. If this value is `$False`, it doesn't wake computers from sleep. For computers to wake, first configure Wake On LAN.

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

### -TaskSequenceDeploymentId

Specifies an ID for a task sequence deployment to configure.

```yaml
Type: String
Parameter Sets: SetTaskSequenceDeploymentByDeploymentIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specifies a name for the task sequence to deploy.

```yaml
Type: String
Parameter Sets: SetTaskSequenceDeploymentByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequencePackageId

Specifies an ID for a task sequence to deploy.

```yaml
Type: String
Parameter Sets: SetTaskSequenceDeploymentByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseMeteredNetwork

Indicates whether to allow clients on a metered internet connection to download content after the installation deadline, which might incur additional costs.

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

Indicates whether client computers use UTC time to determine the availability of a program. UTC time makes the task sequence available at the same time for all computers.

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

Indicates whether client computers use UTC time to determine the expiration of a program. UTC time makes the task sequence available at the same time for all computers.

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

### IResultObject#SMS_Advertisement
## NOTES

## RELATED LINKS

[New-CMTaskSequenceDeployment](./New-CMTaskSequenceDeployment.md)
[Get-CMTaskSequenceDeployment](./Get-CMTaskSequenceDeployment.md)
[Remove-CMTaskSequenceDeployment](./Remove-CMTaskSequenceDeployment.md)
[New-CMSchedule](New-CMSchedule.md)
[Get-CMTaskSequence](Get-CMTaskSequence.md)
