---
description: Changes values that define how Configuration Manager deploys a software package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/30/2018
schema: 2.0.0
title: Set-CMPackageDeployment
---

# Set-CMPackageDeployment

## SYNOPSIS

Changes values that define how Configuration Manager deploys a software package.

## SYNTAX

### SetStandardProgramDeploymentByPackageValue (Default)
```
Set-CMPackageDeployment [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>] [-Comment <String>]
 [-DeploymentAvailableDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-EnableExpireSchedule <Boolean>] [-FastNetworkOption <FastNetworkOptionType>] -InputObject <IResultObject>
 [-PersistOnWriteFilterDevice <Boolean>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType[]>]
 [-SendWakeupPacket <Boolean>] [-SlowNetworkOption <SlowNetworkOptionType>] [-SoftwareInstallation <Boolean>]
 -StandardProgramName <String> [-SystemRestart <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStandardProgramDeploymentByPackageName
```
Set-CMPackageDeployment [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>] [-Comment <String>]
 [-DeploymentAvailableDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-EnableExpireSchedule <Boolean>] [-FastNetworkOption <FastNetworkOptionType>] -PackageName <String>
 [-PersistOnWriteFilterDevice <Boolean>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType[]>]
 [-SendWakeupPacket <Boolean>] [-SlowNetworkOption <SlowNetworkOptionType>] [-SoftwareInstallation <Boolean>]
 -StandardProgramName <String> [-SystemRestart <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStandardProgramDeploymentByPackageId
```
Set-CMPackageDeployment [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>] [-Comment <String>]
 [-DeploymentAvailableDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-EnableExpireSchedule <Boolean>] [-FastNetworkOption <FastNetworkOptionType>] -PackageId <String>
 [-PersistOnWriteFilterDevice <Boolean>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType[]>]
 [-SendWakeupPacket <Boolean>] [-SlowNetworkOption <SlowNetworkOptionType>] [-SoftwareInstallation <Boolean>]
 -StandardProgramName <String> [-SystemRestart <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramDeploymentByPackageName
```
Set-CMPackageDeployment [-Comment <String>] [-DeploymentStartDateTime <DateTime>] -DeviceProgramName <String>
 -PackageName <String> [-RecurUnit <RecurUnitType>] [-RecurValue <Int32>] [-Rerun <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-UseRecurrencePattern <Boolean>] [-UseUtc <Boolean>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramDeploymentByPackageId
```
Set-CMPackageDeployment [-Comment <String>] [-DeploymentStartDateTime <DateTime>] -DeviceProgramName <String>
 -PackageId <String> [-RecurUnit <RecurUnitType>] [-RecurValue <Int32>] [-Rerun <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-UseRecurrencePattern <Boolean>] [-UseUtc <Boolean>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramDeploymentByPackageValue
```
Set-CMPackageDeployment [-Comment <String>] [-DeploymentStartDateTime <DateTime>] -DeviceProgramName <String>
 -InputObject <IResultObject> [-RecurUnit <RecurUnitType>] [-RecurValue <Int32>] [-Rerun <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-UseRecurrencePattern <Boolean>] [-UseUtc <Boolean>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMPackageDeployment** cmdlet changes values that define how Configuration Manager deploys a software package.
A deployment includes a collection of devices or users, a package to deploy, and either a device program name or a standard program name.
To specify which deployment to modify, specify the collection name, package, and program name.
You can specify the package by name or ID, or you can use the [Get-CMPackage](Get-CMPackage.md) cmdlet to get a package object.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set recurrence properties

```powershell
PS XYZ:\> Set-CMPackageDeployment -CollectionName "All Systems" -DeviceProgramName "DPM" -PackageName "User State Migration Tool for Windows 8" -RecurUnit Hours -RecurValue 7 -UseRecurrencePattern $True
```

This command makes changes to the deployment specified by the collection named All Systems, the device program named DPM, and the package named User State Migration Tool for Windows 8.
The command sets the *UseRecurrencePattern* parameter to a value of $True.
The command specifies a recur unit of Hours and a recur value of seven.
Therefore, the deployment recurs every seven hours.

### Example 2: Set availability day and time

```powershell
PS XYZ:\> Set-CMPackageDeployment -CollectionName "All Systems" -PackageName "User State Migration Tool for Windows 8" -StandardProgramName "SPM" -DeploymentAvailableDay 2012/10/18 -DeploymentAvailableTime 15:41 -UseUtcForAvailableSchedule $False
```

This command makes changes to the deployment specified by the collection named All Systems, the package named User State Migration Tool for Windows 8, and the standard program named SPM.
The command specifies a day and time when the deployment becomes available.
The command also specifies that the deployment does not use UTC for the availability schedule.
The schedule refers to the local time zone.

## PARAMETERS

### -AllowFallback
{{ Fill AllowFallback Description }}

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

### -Collection

Specifies the user collection.

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

Specifies the ID of a device or user collection.

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

Specifies the ID of a device or user collection.

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

### -DeploymentAvailableDateTime

Specifies, as a **DateTime** object, the date and time that the deployment becomes available.
To obtain a **DateTime** object, use the Get-Date cmdlet.

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

### -DeploymentExpireDateTime

Specifies, as a **DateTime** object, the date and time that the deployment expires.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.

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

### -DeploymentStartDateTime

Specifies, as a **DateTime** object, the date and time that the deployment starts.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.


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

Specifies a package object.

```yaml
Type: IResultObject
Parameter Sets: SetStandardProgramDeploymentByPackageValue, SetDeviceProgramDeploymentByPackageValue
Aliases: Package, DeploymentSummary, Advertisement

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
Parameter Sets: SetStandardProgramDeploymentByPackageId, SetDeviceProgramDeploymentByPackageId
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

Indicates whether to run from software center.

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

Specifies a **CMSchedule** object.
The schedule specifies when the maintenance window occurs.
To create a **CMSchedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

Indicates whether to send a wake-up packet to computers before the deployment begins.
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
{{ Fill UseMeteredNetwork Description }}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMPackageDeployment](New-CMPackageDeployment.md)
[Get-CMPackageDeployment](Get-CMPackageDeployment.md)
[Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md)
[Remove-CMPackageDeployment](Remove-CMPackageDeployment.md)
[Get-CMPackage](Get-CMPackage.md)
