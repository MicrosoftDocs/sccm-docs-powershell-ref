---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834132
schema: 2.0.0
ms.assetid: BD9CE45B-D225-4A44-9B6F-A819B468CA2E
---

# Set-CMTaskSequenceDeployment

## SYNOPSIS
Creates a task sequence deployment in Configuration Manager.

## SYNTAX

### SetTaskSequenceDeploymentByValueMandatory (Default)
```
Set-CMTaskSequenceDeployment -InputObject <IResultObject> [-CollectionName <String>] [-Comment <String>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-MakeAvailableTo <MakeAvailableToType>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentAvailableDateTime <DateTime>] [-UseUtcForAvailableSchedule <Boolean>]
 [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType[]>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-AllowUsersRunIndependently <Boolean>]
 [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-InternetOption <Boolean>] [-DeploymentOption <DeploymentOptionType>]
 [-AllowSharedContent <Boolean>] [-AllowFallback <Boolean>] [-CreateAlertOnSuccess <Boolean>]
 [-PercentSuccess <Int32>] [-AlertDay <DateTime>] [-AlertTime <DateTime>] [-AlertDateTime <DateTime>]
 [-CreateAlertOnFailure <Boolean>] [-PercentFailure <Int32>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetTaskSequenceDeploymentByNameMandatory
```
Set-CMTaskSequenceDeployment -TaskSequenceName <String> -CollectionName <String> [-Comment <String>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-MakeAvailableTo <MakeAvailableToType>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentAvailableDateTime <DateTime>] [-UseUtcForAvailableSchedule <Boolean>]
 [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType[]>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-AllowUsersRunIndependently <Boolean>]
 [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-InternetOption <Boolean>] [-DeploymentOption <DeploymentOptionType>]
 [-AllowSharedContent <Boolean>] [-AllowFallback <Boolean>] [-CreateAlertOnSuccess <Boolean>]
 [-PercentSuccess <Int32>] [-AlertDay <DateTime>] [-AlertTime <DateTime>] [-AlertDateTime <DateTime>]
 [-CreateAlertOnFailure <Boolean>] [-PercentFailure <Int32>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetTaskSequenceDeploymentByIdMandatory
```
Set-CMTaskSequenceDeployment -TaskSequencePackageId <String> -CollectionName <String> [-Comment <String>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-MakeAvailableTo <MakeAvailableToType>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentAvailableDateTime <DateTime>] [-UseUtcForAvailableSchedule <Boolean>]
 [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType[]>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-AllowUsersRunIndependently <Boolean>]
 [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-InternetOption <Boolean>] [-DeploymentOption <DeploymentOptionType>]
 [-AllowSharedContent <Boolean>] [-AllowFallback <Boolean>] [-CreateAlertOnSuccess <Boolean>]
 [-PercentSuccess <Int32>] [-AlertDay <DateTime>] [-AlertTime <DateTime>] [-AlertDateTime <DateTime>]
 [-CreateAlertOnFailure <Boolean>] [-PercentFailure <Int32>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetTaskSequenceDeploymentByDeploymentIdMandatory
```
Set-CMTaskSequenceDeployment -TaskSequenceDeploymentId <String> [-Comment <String>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-MakeAvailableTo <MakeAvailableToType>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentAvailableDateTime <DateTime>] [-UseUtcForAvailableSchedule <Boolean>]
 [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType[]>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-AllowUsersRunIndependently <Boolean>]
 [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-InternetOption <Boolean>] [-DeploymentOption <DeploymentOptionType>]
 [-AllowSharedContent <Boolean>] [-AllowFallback <Boolean>] [-CreateAlertOnSuccess <Boolean>]
 [-PercentSuccess <Int32>] [-AlertDay <DateTime>] [-AlertTime <DateTime>] [-AlertDateTime <DateTime>]
 [-CreateAlertOnFailure <Boolean>] [-PercentFailure <Int32>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMTaskSequenceDeployment** cmdlet creates a task sequence deployment.
A task sequence deployment assigns a task sequence to a collection of computers.

## EXAMPLES

### Example 1: Create a task sequence deployment
```
PS C:\>Set-CMTaskSequenceDeployment -TaskSequenceName "Task Sequence 1333" -CollectionName "All Systems" -Comment "Task sequence test" -ShowTaskSequenceProgress $True
```

This command creates the task sequence deployment by using the task sequence name and collection name.

### Example 2: Create a task sequence deployment with a task sequence name
```
PS C:\>Set-CMTaskSequenceDeployment -TaskSequenceName "Task Sequence 1333" -CollectionName "All Desktop and Server Clients" -Comment "Task sequence test" -SendWakeUpPacket $True -UseMeteredNetwork $True -DeploymentExpireDay 2014/12/30 -DeploymentExpireTime 15:52 -UseUtcForExpireSchedule $True -ScheduleEvent LogOff -RerunBehavior NeverRerunDeployedProgram -AllowUsersRunIndependently $True -ShowTaskSequenceProgress $False -SoftwareInstallation $True -SystemRestart $True -PersistOnWriteFilterDevice $False -InternetOption $True -DeploymentOption DownloadAllContentLocallyBeforeStartingTaskSequence -AllowFallback $True -AllowSharedContent $True -CreatAlertBaseOnPercentSuccess $True -CreatAlertBaseOnPercentFailure $True
```

This command creates the task sequence deployment by using the task sequence name and collection name.

## PARAMETERS

### -AlertDateTime


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

### -AlertDay
Specifies a day, in MM/DD/YYYY format, to trigger alerts.
If you configure a percent success or failure rate for a deployment, alerts appear after this date.

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

### -AlertTime
Specifies a time, in HH:MM format, to trigger alerts.
If you configure a percent success or failure rate for a deployment, alerts appear after this time.

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

### -CollectionName
Specifies a name of a collection designated to receive a task sequence deployment.
A collection is a group of client computers.

```yaml
Type: String
Parameter Sets: SetTaskSequenceDeploymentByValueMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetTaskSequenceDeploymentByNameMandatory, SetTaskSequenceDeploymentByIdMandatory
Aliases: 
Required: True
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateAlertOnFailure


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

### -DeploymentAvailableDay
Specifies a day, in MM/DD/YYYY format, when a deployment becomes available to clients.
By default, the deployment becomes available immediately.

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

### -DeploymentAvailableTime
Specifies a time, in HH:MM format, when a deployment becomes available to clients.
By default, the deployment becomes available immediately.

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

### -DeploymentExpireDay
Specifies a day, in MM/DD/YYYY format, when a deployment expires.
By default, a deployment never expires.
To expire a deployment on a certain day, set this parameter.
You may use this parameter in conjunction with the *DeploymentExpireTime* parameter.

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

### -DeploymentExpireTime
Specifies a time, in HH:MM format, when the deployment expires.
By default, a deployment never expires.
To expire a deployment at a certain time, set this parameter.
You may use this parameter in conjunction with the *DeploymentExpireDay* parameter.

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
By default, clients download content as needed.
The acceptable values for this parameter are:

- DownloadAllContentLocallyBeforeStartingTaskSequence
- DownloadContentLocallyWhenNeededByRunningTaskSequence

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

### -InputObject
Specifies an task sequence deployment object.
To obtain a task sequence object, use the [Get-CMTaskSequenceDeployment](./Get-CMTaskSequenceDeployment.md) cmdlet.


```yaml
Type: IResultObject
Parameter Sets: SetTaskSequenceDeploymentByValueMandatory
Aliases: Deployment, TaskSequence
Required: True
Position: Named
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

### -MakeAvailableTo
Specifies whether to make this task sequence available to Configuration Manager clients, and whether to make it available when you deploy an operating system by using boot media, prestaged media, or PXE.
The acceptable values for this parameter are:

- Clients
- ClientsMediaAndPxe
- MediaAndPxe
- MediaAndPxeHidden

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
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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
The acceptable values for this parameter are:

- AlwaysRerunProgram
- NeverRerunDeployedProgram
- RerunIfFailedPreviousAttempt
- RerunIfSucceededOnPreviousAttempt

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
Specifies an array of **CMSchedule** objects.
A **CMSchedule** object defines the mandatory assignment schedule for a deployment.
To create a **CMSchedule** object, use the [New-CMSchedule](./New-CMSchedule.md) cmdlet.

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
Indicates whether to send a wake up packet to computers before the deployment begins.
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

### -TaskSequenceDeploymentId
Specifies an ID for a task sequence deployment.

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
Specifies a name for a task sequence.

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
Specifies an ID for a task sequence package.

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

[Start-CMTaskSequenceDeployment](./Start-CMTaskSequenceDeployment.md)

[New-CMSchedule](./New-CMSchedule.md)

[Get-CMTaskSequence](./Get-CMTaskSequence.md)
