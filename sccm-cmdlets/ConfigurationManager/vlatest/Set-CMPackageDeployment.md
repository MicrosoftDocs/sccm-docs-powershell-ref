---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833979
schema: 2.0.0
ms.assetid: 6814743B-10B2-4A47-9BCD-7E52B54CC444
---

# Set-CMPackageDeployment

## SYNOPSIS
Changes values that define how Configuration Manager deploys a software package.

## SYNTAX

### SetStandardProgramDeploymentByPackageValue (Default)
```
Set-CMPackageDeployment -Package <IResultObject> -StandardProgramName <String> -CollectionName <String>
 [-Comment <String>] [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-UseUtcForAvailableSchedule <Boolean>] [-EnableExpireSchedule <Boolean>] [-DeploymentExpireDay <DateTime>]
 [-DeploymentExpireTime <DateTime>] [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType[]>]
 [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>]
 [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-FastNetworkOption <FastNetworkOptionType>] [-SlowNetworkOption <SlowNetworkOptionType>]
 [-AllowSharedContent <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetStandardProgramDeploymentByPackageName
```
Set-CMPackageDeployment -PackageName <String> -StandardProgramName <String> -CollectionName <String>
 [-Comment <String>] [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-UseUtcForAvailableSchedule <Boolean>] [-EnableExpireSchedule <Boolean>] [-DeploymentExpireDay <DateTime>]
 [-DeploymentExpireTime <DateTime>] [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType[]>]
 [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>]
 [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-FastNetworkOption <FastNetworkOptionType>] [-SlowNetworkOption <SlowNetworkOptionType>]
 [-AllowSharedContent <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDeviceProgramDeploymentByPackageName
```
Set-CMPackageDeployment -PackageName <String> -DeviceProgramName <String> -CollectionName <String>
 [-Comment <String>] [-UseMeteredNetwork <Boolean>] [-DeploymentStartDay <DateTime>]
 [-DeploymentStartTime <DateTime>] [-UseUtc <Boolean>] [-UseRecurrencePattern <Boolean>] [-RecurValue <Int32>]
 [-RecurUnit <RecurUnitType>] [-Rerun <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramDeploymentByPackageId
```
Set-CMPackageDeployment -PackageId <String> -DeviceProgramName <String> -CollectionName <String>
 [-Comment <String>] [-UseMeteredNetwork <Boolean>] [-DeploymentStartDay <DateTime>]
 [-DeploymentStartTime <DateTime>] [-UseUtc <Boolean>] [-UseRecurrencePattern <Boolean>] [-RecurValue <Int32>]
 [-RecurUnit <RecurUnitType>] [-Rerun <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetStandardProgramDeploymentByPackageId
```
Set-CMPackageDeployment -PackageId <String> -StandardProgramName <String> -CollectionName <String>
 [-Comment <String>] [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-UseUtcForAvailableSchedule <Boolean>] [-EnableExpireSchedule <Boolean>] [-DeploymentExpireDay <DateTime>]
 [-DeploymentExpireTime <DateTime>] [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType[]>]
 [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>]
 [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-FastNetworkOption <FastNetworkOptionType>] [-SlowNetworkOption <SlowNetworkOptionType>]
 [-AllowSharedContent <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDeviceProgramDeploymentByPackageValue
```
Set-CMPackageDeployment -Package <IResultObject> -DeviceProgramName <String> -CollectionName <String>
 -Comment <String> [-UseMeteredNetwork <Boolean>] [-DeploymentStartDay <DateTime>]
 [-DeploymentStartTime <DateTime>] [-UseUtc <Boolean>] [-UseRecurrencePattern <Boolean>] [-RecurValue <Int32>]
 [-RecurUnit <RecurUnitType>] [-Rerun <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMPackageDeployment** cmdlet changes values that define how Microsoft System Center Configuration Manager deploys a software package.
A deployment includes a collection of devices or users, a package to deploy, and either a device program name or a standard program name.
To specify which deployment to modify, specify the collection name, package, and program name.
You can specify the package by name or ID, or you can use the Get-CMPackage cmdlet to get a package object.

## EXAMPLES

### Example 1: Set recurrence properties
```
PS C:\>Set-CMPackageDeployment -CollectionName "All Systems" -DeviceProgramName "DPM" -PackageName "User State Migration Tool for Windows 8" -RecurUnit Hours -RecurValue 7 -UseRecurrencePattern $True
```

This command makes changes to the deployment specified by the collection named All Systems, the device program named DPM, and the package named User State Migration Tool for Windows 8.
The command sets the *UseRecurrencePattern* parameter to a value of $True.
The command specifies a recur unit of Hours and a recur value of seven.
Therefore, the deployment recurs every seven hours.

### Example 2: Set availability day and time
```
PS C:\>Set-CMPackageDeployment -CollectionName "All Systems" -PackageName "User State Migration Tool for Windows 8" -StandardProgramName "SPM" -DeploymentAvailableDay 2012/10/18 -DeploymentAvailableTime 15:41 -UseUtcForAvailableSchedule $False
```

This command makes changes to the deployment specified by the collection named All Systems, the package named User State Migration Tool for Windows 8, and the standard program named SPM.
The command specifies a day and time when the deployment becomes available.
The command also specifies that the deployment does not use UTC for the availability schedule.
The schedule refers to the local time zone.

## PARAMETERS

### -AllowSharedContent
Indicates whether clients use shared content.
If this value is $True, clients attempt to download content from other clients that downloaded that content.
If this value is $False, clients do not attempt to download from other clients.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the ID of a device or user collection.

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

### -Comment
Specifies a comment for the deployment.

```yaml
Type: String
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetDeviceProgramDeploymentByPackageValue
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

### -DeploymentAvailableDay
Specifies a day as a **DateTime** object.
To obtain a **DateTime** object, use the Get-Date cmdlet.
For more information, type `Get-Help Get-Date`.
This is the day on which the deployment becomes available.
If you specify a value for the *DeployAvailableTime* parameter in addition to this parameter, the cmdlet uses that value.

```yaml
Type: DateTime
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentAvailableTime
Specifies a time as a **DateTime** object.
This is the time at which the deployment becomes available.

```yaml
Type: DateTime
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentExpireDay
Specifies a day as a **DateTime** object.
This is the day on which the deployment expires.
If you specify a value for the *DeploymentExpireTime* parameter in addition to this parameter, the cmdlet uses that value.

```yaml
Type: DateTime
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentExpireTime
Specifies a time as a **DateTime** object.
This is the time at which the deployment expires.

```yaml
Type: DateTime
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentStartDay
Specifies a day as a **DateTime** object.
This is the day on which the deployment starts.
If you specify a value for the *DeploymentStartTime* parameter in addition to this parameter, the cmdlet uses that value.

```yaml
Type: DateTime
Parameter Sets: SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentStartTime
Specifies a time as a **DateTime** object.
This is the time at which the deployment starts.

```yaml
Type: DateTime
Parameter Sets: SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceProgramName
Specifies the name of a device program.

```yaml
Type: String
Parameter Sets: SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Required: True
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

### -EnableExpireSchedule
Indicates whether to enable the schedule to expire the deployment.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FastNetworkOption
Specifies client behavior on a fast network.
The acceptable values for this parameter are:

- DownloadContentFromDistributionPointAndRunLocally
- RunProgramFromDistributionPoint

```yaml
Type: FastNetworkOptionType
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Accepted values: RunProgramFromDistributionPoint, DownloadContentFromDistributionPointAndRunLocally
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

### -Package
Specifies a package object.
To obtain a package object, use the Get-CMPackage cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PackageId
Specifies the ID of a package.

```yaml
Type: String
Parameter Sets: SetDeviceProgramDeploymentByPackageId, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName
Specifies the name of a package.

```yaml
Type: String
Parameter Sets: SetStandardProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistOnWriteFilterDevice
Indicates whether to enable write filters for embedded devices.
For a value of $True, the device commits changes during a maintenance window.
This action requires a restart.
For a value of $False, the device saves changes in an overlay and commits them later.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurUnit
Specifies a unit for a recurring deployment.
The acceptable values for this parameter are:

- Days
- Hours
- Minutes

```yaml
Type: RecurUnitType
Parameter Sets: SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Accepted values: Minutes, Hours, Days
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurValue
Specifies how often a deployment recurs.
This parameter depends on the unit type specified in the *RecurUnit* parameter.
This value can be between 1 and 23 if the unit is Hours, between 1 and 31 if the unit is Days, or between 1 and 59 if the unit is Minutes.

```yaml
Type: Int32
Parameter Sets: SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rerun
Indicates whether the deployment reruns.
If this value is $True, the deployment runs again for clients as specified in the *RerunBehavior* parameter.
If this value is $False, the deployment does not run again.

```yaml
Type: Boolean
Parameter Sets: SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RerunBehavior
Specifies how a deployment reruns on a client.
The acceptable values for this parameter are:

- AlwaysRerunProgram.
Rerun as scheduled, even if the deployment succeeded.
You can use this value for recurring deployments. 
- NeverRerunDeployedProgram.
Does not rerun, even if the deployment failed or files changed. 
- RerunIfFailedPreviousAttempt.
Rerun, as scheduled, if the deployment failed on the previous attempt. 
- RerunIfSucceededOnpreviousAttempt.
Rerun only if the previous attempt succeeded.
You can use this value for updates that depend on the previous update.

```yaml
Type: RerunBehaviorType
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
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
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: AllowUsersRunIndependently
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies an array of schedule objects for the deployment.

```yaml
Type: IResultObject[]
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScheduleEvent
Specifies an array of schedule event types.
The acceptable values for this parameter are:

- AsSoonAsPossible
- LogOff
- LogOn
- SendWakeUpPacket

```yaml
Type: ScheduleEventType[]
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
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
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SlowNetworkOption
Specifies how Configuration Manager deploys this package in a slow network.
The acceptable values for this parameter are:

- DoNotRunProgram
- DownloadContentFromDistributionPointAndLocally
- RunProgramFromDistributionPoint

```yaml
Type: SlowNetworkOptionType
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Accepted values: DoNotRunProgram, DownloadContentFromDistributionPointAndLocally, RunProgramFromDistributionPoint
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInstallation
Indicates whether to install the deployed software outside of maintenance windows.
A maintenance window is a specified period of time used for computer maintenance and updates.
If this value is $True, the Configuration Manager installs software according to schedule, even if the schedule falls outside a maintenance window.
If this value is $False, Configuration Manager does not install deployed software outside any windows, but waits for a maintenance window.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardProgramName
Specifies a standard program name.

```yaml
Type: String
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemRestart
Indicates whether a system restarts outside a maintenance window.
A maintenance window is a specified period of time used for computer maintenance and updates.
If this value is $True, any required restart takes place without regard to maintenance windows.
If this value is $False, the computer does not restart outside a maintenance window.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseMeteredNetwork
Indicates whether to allow clients to download content over a metered Internet connection after the deadline, which may incur additional expense.

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

### -UseRecurrencePattern
Indicates whether to use a recurrence pattern.

```yaml
Type: Boolean
Parameter Sets: SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtc
Indicates whether to use Coordinated Universal Time (UTC), also known as Greenwich Mean Time.
If this value is $True, Configuration Manager uses UTC for this deployment.
If this value is $False, Configuration Manager uses local time.

```yaml
Type: Boolean
Parameter Sets: SetDeviceProgramDeploymentByPackageName, SetDeviceProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageValue
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtcForAvailableSchedule
Indicates whether to use UTC for available schedule.
If this value is $True, Configuration Manager uses UTC.
If this value is $False, Configuration Manager uses local time.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtcForExpireSchedule
Indicates whether to use UTC for expire schedule.
If this value is $True, Configuration Manager uses UTC.
If this value is $False, Configuration Manager uses local time.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetStandardProgramDeploymentByPackageName, SetStandardProgramDeploymentByPackageId
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

[Start-CMPackageDeployment](./Start-CMPackageDeployment.md)

[Get-CMPackage](./Get-CMPackage.md)


