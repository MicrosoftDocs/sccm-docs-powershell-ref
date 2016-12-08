---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834231
schema: 2.0.0
ms.assetid: 83C8EA1B-C6A1-4962-BEB9-409EB24305F5
---

# Start-CMTaskSequenceDeployment

## SYNOPSIS
Starts a task sequence deployment in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Start-CMTaskSequenceDeployment [-InputObject] <IResultObject> [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-Comment <String>]
 [-DeployPurpose <DeployPurposeType>] [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-Availability <MakeAvailableToType>] [-DeploymentAvailableDay <DateTime>]
 [-DeploymentAvailableTime <DateTime>] [-DeploymentAvailableDateTime <DateTime>]
 [-UseUtcForAvailableSchedule <Boolean>] [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>]
 [-DeploymentExpireDateTime <DateTime>] [-UseUtcForExpireSchedule <Boolean>]
 [-ScheduleEvent <ScheduleEventType[]>] [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>] [-InternetOption <Boolean>]
 [-CreateAlertOnSuccess <Boolean>] [-PercentSuccess <Int32>] [-AlertDay <DateTime>] [-AlertTime <DateTime>]
 [-AlertDateTime <DateTime>] [-CreateAlertOnFailure <Boolean>] [-PercentFailure <Int32>]
 [-DeploymentOption <DeploymentOptionType>] [-AllowSharedContent <Boolean>] [-AllowFallback <Boolean>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Start-CMTaskSequenceDeployment [-TaskSequencePackageId] <String> [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-Comment <String>]
 [-DeployPurpose <DeployPurposeType>] [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-Availability <MakeAvailableToType>] [-DeploymentAvailableDay <DateTime>]
 [-DeploymentAvailableTime <DateTime>] [-DeploymentAvailableDateTime <DateTime>]
 [-UseUtcForAvailableSchedule <Boolean>] [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>]
 [-DeploymentExpireDateTime <DateTime>] [-UseUtcForExpireSchedule <Boolean>]
 [-ScheduleEvent <ScheduleEventType[]>] [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>] [-InternetOption <Boolean>]
 [-CreateAlertOnSuccess <Boolean>] [-PercentSuccess <Int32>] [-AlertDay <DateTime>] [-AlertTime <DateTime>]
 [-AlertDateTime <DateTime>] [-CreateAlertOnFailure <Boolean>] [-PercentFailure <Int32>]
 [-DeploymentOption <DeploymentOptionType>] [-AllowSharedContent <Boolean>] [-AllowFallback <Boolean>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMTaskSequenceDeployment** cmdlet starts a task sequence deployment.
A task sequence deployment assigns a task sequence to a collection of computers.

## EXAMPLES

### Example 1: Start a task sequence deployment
```
PS C:\> Start-CMTaskSequenceDeployment -Name "Task Sequence 1333" -CollectionName "All Systems"
```

This command starts a task sequence deployment by using the name of the task sequence deployment and the name of a collection.

### Example 2: Start a task sequence deployment for devices
```
PS C:\> Start-CMTaskSequenceDeployment -Name "Task Sequence 1333" -CollectionName "All Mobile Devices" -Comment "Task sequence test" -DeployPurpose Required -SendWakeUpPacket $True -UseMeteredNetwork $True -ScheduleEvent AsSoonAsPossible -RerunBehavior NeverRerunDeployedProgram -AllowUsersRunIndependently $True -ShowTaskSequenceProgress $False -SoftwareInstallation $True -SystemRestart $True -PersistOnWriteFilterDevice $False -AllowFallback $True -CreatAlertBaseOnPercentSuccess $True -CreatAlertBaseOnPercentFailure $True -DeploymentOption DownloadAllContentLocallyBeforeStartingTaskSequence -AllowSharedContent $True -InternetOption $True
```

This command starts a task sequence deployment for mobile devices.
The command does not allow the use of the *PersistOnWriteFilterDevice* parameter.

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
Specifies a day, in MM/DD/YYYY format, to notify clients of a new deployment.

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
Specifies a time, in HH:MM format, to notify clients of a new deployment.

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
Indicates whether to allow a fallback status point for clients.

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
Indicates whether to allow shared content, such as a shared network folder.

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

### -DeployPurpose
Specifies a task sequence as either required or available.
A required task sequence installation is mandatory.
The acceptable values for this parameter are:

- Available
- Required

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
To have a deployment expire on a certain day, set this parameter.

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
To have a deployment expire at a certain time, set this parameter.

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
Specifies a task sequence deployment object.

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
Specifies a percentage for failed task sequence deployment.

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
Specifies a percentage for successful task sequence deployment.

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

### -RunFromSoftwareCenter


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
Specifies an array of schedule objects.

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
The *Purpose* parameter must be set to Required.

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
Specifies an array of IDs for a task sequence package.

```yaml
Type: String
Parameter Sets: SearchPackageByIdMandatory
Aliases: PackageId
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseMeteredNetwork
Indicates whether to allow clients to connect to a metered network to download a program.

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

[Set-CMTaskSequenceDeployment](./Set-CMTaskSequenceDeployment.md)


