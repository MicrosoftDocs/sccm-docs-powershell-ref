---
external help file: AdminUI.PS.AppModel.dll-Help.xml
ms.assetid: 97AD7791-97A7-492A-BD08-274EDAED0F2B
online version: https://go.microsoft.com/fwlink/?linkid=834222
schema: 2.0.0
---

# Start-CMPackageDeployment

## SYNOPSIS
Starts deployment of a software package to a Configuration Manager collection.

## SYNTAX

### DeployStandardProgramByPackageValue (Default)
```
Start-CMPackageDeployment [-StandardProgram] [-Package] <IResultObject> -ProgramName <String>
 -CollectionName <String> [-Comment <String>] [-DeployPurpose <DeployPurposeType>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-DeploymentAvailableDay <DateTime>]
 [-DeploymentAvailableTime <DateTime>] [-DeploymentAvailableDateTime <DateTime>]
 [-UseUtcForAvailableSchedule <Boolean>] [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>]
 [-DeploymentExpireDateTime <DateTime>] [-UseUtcForExpireSchedule <Boolean>]
 [-ScheduleEvent <ScheduleEventType>] [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-FastNetworkOption <FastNetworkOptionType>]
 [-SlowNetworkOption <SlowNetworkOptionType>] [-AllowSharedContent <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageName
```
Start-CMPackageDeployment [-DeviceProgram] -PackageName <String> -ProgramName <String> -CollectionName <String>
 [-Comment <String>] [-DeployPurpose <DeployPurposeType>] [-UseMeteredNetwork <Boolean>]
 [-DeploymentStartDay <DateTime>] [-DeploymentStartTime <DateTime>] [-DeploymentStartDateTime <DateTime>]
 [-UseUtc <Boolean>] [-RecurValue <Int32>] [-RecurUnit <RecurUnitType>] [-Rerun <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageId
```
Start-CMPackageDeployment [-DeviceProgram] -PackageId <String> -ProgramName <String> -CollectionName <String>
 [-Comment <String>] [-DeployPurpose <DeployPurposeType>] [-UseMeteredNetwork <Boolean>]
 [-DeploymentStartDay <DateTime>] [-DeploymentStartTime <DateTime>] [-DeploymentStartDateTime <DateTime>]
 [-UseUtc <Boolean>] [-RecurValue <Int32>] [-RecurUnit <RecurUnitType>] [-Rerun <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageValue
```
Start-CMPackageDeployment [-DeviceProgram] [-Package] <IResultObject> -ProgramName <String>
 -CollectionName <String> [-Comment <String>] [-DeployPurpose <DeployPurposeType>]
 [-UseMeteredNetwork <Boolean>] [-DeploymentStartDay <DateTime>] [-DeploymentStartTime <DateTime>]
 [-DeploymentStartDateTime <DateTime>] [-UseUtc <Boolean>] [-RecurValue <Int32>] [-RecurUnit <RecurUnitType>]
 [-Rerun <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeployDeviceProgramByProgramValue
```
Start-CMPackageDeployment [-DeviceProgram] [-Program] <IResultObject> -CollectionName <String>
 [-Comment <String>] [-DeployPurpose <DeployPurposeType>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-DeploymentStartDay <DateTime>] [-DeploymentStartTime <DateTime>]
 [-DeploymentStartDateTime <DateTime>] [-UseUtc <Boolean>] [-RecurValue <Int32>] [-RecurUnit <RecurUnitType>]
 [-Rerun <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeployStandardProgramByPackageName
```
Start-CMPackageDeployment [-StandardProgram] -PackageName <String> -ProgramName <String>
 -CollectionName <String> [-Comment <String>] [-DeployPurpose <DeployPurposeType>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-DeploymentAvailableDay <DateTime>]
 [-DeploymentAvailableTime <DateTime>] [-DeploymentAvailableDateTime <DateTime>]
 [-UseUtcForAvailableSchedule <Boolean>] [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>]
 [-DeploymentExpireDateTime <DateTime>] [-UseUtcForExpireSchedule <Boolean>]
 [-ScheduleEvent <ScheduleEventType>] [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-FastNetworkOption <FastNetworkOptionType>]
 [-SlowNetworkOption <SlowNetworkOptionType>] [-AllowSharedContent <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployStandardProgramByPackageId
```
Start-CMPackageDeployment [-StandardProgram] -PackageId <String> -ProgramName <String> -CollectionName <String>
 [-Comment <String>] [-DeployPurpose <DeployPurposeType>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentAvailableDateTime <DateTime>] [-UseUtcForAvailableSchedule <Boolean>]
 [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-FastNetworkOption <FastNetworkOptionType>] [-SlowNetworkOption <SlowNetworkOptionType>]
 [-AllowSharedContent <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployStandardProgramByProgramValue
```
Start-CMPackageDeployment [-StandardProgram] [-Program] <IResultObject> -CollectionName <String>
 [-Comment <String>] [-DeployPurpose <DeployPurposeType>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentAvailableDateTime <DateTime>] [-UseUtcForAvailableSchedule <Boolean>]
 [-DeploymentExpireDay <DateTime>] [-DeploymentExpireTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-FastNetworkOption <FastNetworkOptionType>] [-SlowNetworkOption <SlowNetworkOptionType>]
 [-AllowSharedContent <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMPackageDeployment** cmdlet starts deployment of a specified software package to computers that belong to a Microsoft System Center Configuration Manager collection.
You can choose when the package becomes available and when the package deployment expires.
You can specify whether System Center Configuration Manager deploys the package only once or repeatedly and what happens when installation fails for a computer.

## EXAMPLES

### Example 1: Start a recurring deployment
```
PS C:\> Start-CMPackageDeployment -CollectionName "All Systems" -DeviceProgramName "DPM" -PackageName "User State Migration Tool for Windows 8" -Comment "DPM for all systems." -DeploymentStartDay 2012/10/26 -DeploymentStartTime 12:12 -RecurUnit Days -RecurValue 7 -Rerun $True -UseMeteredNetwork $True -UseUtc $True
```

This command starts deployment for a named package to the collection named All Systems for the device program named DPM.
The command specifies a start day and start time.
The command includes a descriptive comment.
The *Rerun* parameter has a value of $True and the command specifies a recur value of seven and a recur unit of Days, so deployment reruns every seven days.
The deployment uses metered network.
The deployment uses UTC time.

### Example 2: Start a recurring deployment for an available package
```
PS C:\> Start-CMPackageDeployment -CollectionName "Western Computers" -DeviceProgramName "DPM" -PackageName "User State Migration Tool for Windows 8" -Comment "Deployment for Western office." -DeployPurpose Available -Rerun $True -UseUtc $True
```

This command starts deployment for a named package to the collection named Western Computers for the device program named DPM.
The command includes a descriptive comment.
The command specifies Available as the *DeployPurpose*, therefor users can decide whether to install this software.
The *Rerun* parameter has a value of $True.
The deployment uses UTC time.

### Example 3: Start a deployment for a standard program
```
PS C:\> Start-CMPackageDeployment -CollectionName "All Systems" -PackageName "User State Migration Tool for Windows 8" -StandardProgramName "SPM" AllowSharedContent $False
```

This command starts a deployment of a package named User State Migration Tool for Windows 8 to the collection named All Systems for the standard program named SPM.
The command does not allow computers to use shared content.

## PARAMETERS

### -AllowSharedContent
Indicates whether clients use shared content.
If this value is $True, clients attempt to download content from other clients that downloaded that content.
If this value is $False, clients do not attempt to download from other clients.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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

### -DeployPurpose
Specifies the purpose for the deployment.
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
Specifies, as a **DateTime** object, the date and time that the deployment becomes available.
To obtain a **DateTime** object, use the Get-Date cmdlet.

```yaml
Type: DateTime
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentAvailableDay
Obsolete.
Use *DeploymentAvailableDateTime*.

```yaml
Type: DateTime
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentAvailableTime
Obsolete.
Use *DeploymentAvailableDateTime*.

```yaml
Type: DateTime
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentExpireDateTime
Specifies, as a **DateTime** object, the date and time that the deployment expires.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.

```yaml
Type: DateTime
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentExpireDay
Obsolete.
Use *DeploymentExpireDateTime*.

```yaml
Type: DateTime
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentExpireTime
Obsolete.
Use *DeploymentExpireDateTime*.

```yaml
Type: DateTime
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentStartDateTime
Specifies, as a **DateTime** object, the date and time that the deployment starts.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.

```yaml
Type: DateTime
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentStartDay
Obsolete.
Use *DeploymentStartDateTime*.

```yaml
Type: DateTime
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentStartTime
Obsolete.
Use *DeploymentStartDateTime*.

```yaml
Type: DateTime
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceProgram
```yaml
Type: SwitchParameter
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 

Required: True
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

### -FastNetworkOption
Specifies client behavior on a fast network.
The acceptable values for this parameter are:

- DownloadContentFromDistributionPointAndRunLocally
- RunProgramFromDistributionPoint

```yaml
Type: FastNetworkOptionType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 
Accepted values: RunProgramFromDistributionPoint, DownloadContentFromDistributionPointAndRunLocally

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

### -Package
Specifies a package object.
To obtain a package object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: DeployStandardProgramByPackageValue, DeployDeviceProgramByPackageValue
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PackageId
Specifies the ID of a package.

```yaml
Type: String
Parameter Sets: DeployDeviceProgramByPackageId, DeployStandardProgramByPackageId
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
Parameter Sets: DeployDeviceProgramByPackageName, DeployStandardProgramByPackageName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
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

### -PersistOnWriteFilterDevice
Indicates whether to enable write filters for embedded devices.
For a value of $True, the device commits changes during a maintenance window.
This action requires a restart.
For a value of $False, the device saves changes in an overlay and commits them later.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Program
```yaml
Type: IResultObject
Parameter Sets: DeployDeviceProgramByProgramValue, DeployStandardProgramByProgramValue
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProgramName
```yaml
Type: String
Parameter Sets: DeployStandardProgramByPackageValue, DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId
Aliases: StandardProgramName, DeviceProgramName

Required: True
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
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
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
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
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
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
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
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 
Accepted values: NeverRerunDeployedProgram, AlwaysRetunProgram, AlwaysRerunProgram, RerunIfFailedPreviousAttempt, RerunIfSucceededOnPreviousAttempt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunFromSoftwareCenter
```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: AllowUsersRunIndependently

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a schedule object for the deployment.

```yaml
Type: IResultObject[]
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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
Type: ScheduleEventType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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
Parameter Sets: DeployStandardProgramByPackageValue, DeployDeviceProgramByProgramValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardProgram
Indicates that the program type in the deployment package is standard program.

```yaml
Type: SwitchParameter
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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

### -UseUtc
Indicates whether to use Coordinated Universal Time (UTC), also known as Greenwich Mean Time.
If this value is $True, Configuration Manager uses UTC for this deployment.
If this value is $False, Configuration Manager uses local time.

```yaml
Type: Boolean
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
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
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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

[Set-CMPackageDeployment](Set-CMPackageDeployment.md)

[Get-CMPackage](Get-CMPackage.md)
