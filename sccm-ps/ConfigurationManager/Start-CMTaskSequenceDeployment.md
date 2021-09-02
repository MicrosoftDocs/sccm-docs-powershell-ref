---
description: Start a task sequence deployment
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/23/2020
schema: 2.0.0
title: Start-CMTaskSequenceDeployment
---

# Start-CMTaskSequenceDeployment

## SYNOPSIS

(Deprecated) Start a task sequence deployment.

## SYNTAX

### SearchByValueMandatory (Default)
```
Start-CMTaskSequenceDeployment [-AlertDateTime <DateTime>] [-AlertDay <DateTime>] [-AlertTime <DateTime>]
 [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>] [-Availability <MakeAvailableToType>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-Comment <String>]
 [-DeploymentAvailableDateTime <DateTime>] [-DeploymentAvailableDay <DateTime>]
 [-DeploymentAvailableTime <DateTime>] [-DeploymentExpireDateTime <DateTime>] [-DeploymentExpireDay <DateTime>]
 [-DeploymentExpireTime <DateTime>] [-DeploymentOption <DeploymentOptionType>]
 [-DeployPurpose <DeployPurposeType>] [-InputObject] <IResultObject> [-InternetOption <Boolean>] [-PassThru]
 [-PercentFailure <Int32>] [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>]
 [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>]
 [-ScheduleEvent <ScheduleEventType[]>] [-SendWakeupPacket <Boolean>] [-ShowTaskSequenceProgress <Boolean>]
 [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Start-CMTaskSequenceDeployment [-AlertDateTime <DateTime>] [-AlertDay <DateTime>] [-AlertTime <DateTime>]
 [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>] [-Availability <MakeAvailableToType>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-Comment <String>]
 [-DeploymentAvailableDateTime <DateTime>] [-DeploymentAvailableDay <DateTime>]
 [-DeploymentAvailableTime <DateTime>] [-DeploymentExpireDateTime <DateTime>] [-DeploymentExpireDay <DateTime>]
 [-DeploymentExpireTime <DateTime>] [-DeploymentOption <DeploymentOptionType>]
 [-DeployPurpose <DeployPurposeType>] [-InternetOption <Boolean>] [-PassThru] [-PercentFailure <Int32>]
 [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType[]>]
 [-SendWakeupPacket <Boolean>] [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-TaskSequencePackageId] <String> [-UseMeteredNetwork <Boolean>]
 [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!IMPORTANT]
> This cmdlet is deprecated. Use [New-CMTaskSequenceDeployment](New-CMTaskSequenceDeployment.md) instead.

Use this cmdlet to start a task sequence deployment. A task sequence deployment assigns a task sequence to a collection of computers. For more information, see [Deploy a task sequence in Configuration Manager](/mem/configmgr/osd/deploy-use/deploy-a-task-sequence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Start a task sequence deployment with default options

This command starts a task sequence deployment by using the name of the task sequence deployment and the name of a collection.

```powershell
Get-CMTaskSequence -Name "Upgrade Windows 10" | Start-CMTaskSequenceDeployment -CollectionName "Collection 01"
```

### Example 2: Start a task sequence deployment with configured options

This command starts a task sequence deployment with several configured options.

```powershell
Start-CMTaskSequenceDeployment -TaskSequencePackageId "XYZ00003" -CollectionName "Collection 02" -Comment "Task sequence test" -DeployPurpose Required -SendWakeUpPacket $True -UseMeteredNetwork $True -ScheduleEvent AsSoonAsPossible -RerunBehavior NeverRerunDeployedProgram -RunFromSoftwareCenter $True -ShowTaskSequenceProgress $False -SoftwareInstallation $True -SystemRestart $True -PersistOnWriteFilterDevice $False -AllowFallback $True -DeploymentOption DownloadAllContentLocallyBeforeStartingTaskSequence -AllowSharedContent $True -InternetOption $True
```

## PARAMETERS

### -AlertDateTime

When you configure the deployment to create an alert for successful deployment, use this parameter to specify a **DateTime** object. Configuration Manager creates a deployment alert when the threshold is lower than the **PercentSuccess** after this date.

To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

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

This parameter is deprecated. Use **AlertDateTime**.

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

This parameter is deprecated. Use **AlertDateTime**.

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

Allow clients to use distribution points from the default site boundary group.

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

Allow clients to use distribution points from a neighbor boundary group.

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

Specify whether to make this task sequence available to Configuration Manager clients, and whether it's available to run when you deploy an OS by using boot media, prestaged media, or PXE.

If you specify `Clients`, the default value for the **DeploymentOption** parameter is `DownloadAllContentLocallyBeforeStartingTaskSequence`.
If you specify `ClientsMediaAndPxe`, `MediaAndPxe`, or `MediaAndPxeHidden`, the default value for the **DeploymentOption** parameter is `DownloadContentLocallyWhenNeededByRunningTaskSequence`.

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

Specify a collection object to which this task sequence is deployed. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify the ID of the collection to which this task sequence is deployed.

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

Specify the name of the collection to which this task sequence is deployed.

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

Specify an optional comment for the task sequence deployment.

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

Specify a **DateTime** object for when this deployment is _available_. To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

Use **DeploymentExpireDateTime** to specify when the deployment _expires_, and **Schedule** to specify the deployment assignment, or _deadline_.

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

This parameter is deprecated. Use **DeploymentAvailableDateTime**.

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

This parameter is deprecated. Use **DeploymentAvailableDateTime**.

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

Specify a **DateTime** object for when this deployment _expires_. To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

Use **DeploymentAvailableDateTime** to specify when the deployment is _available_, and **Schedule** to specify the deployment assignment, or _deadline_.

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

This parameter is deprecated. Use **DeploymentExpireDateTime**.

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

This parameter is deprecated. Use **DeploymentExpireDateTime**.

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

Specify how clients interact with the distribution points to get content for the task sequence. Not all options are available in specific scenarios. For more information, see [Deploy a task sequence - Deployment options](/mem/configmgr/osd/deploy-use/deploy-a-task-sequence#bkmk_deploy-options).

If you specify `Clients` for the **Availability** parameter, the default value for this parameter is `DownloadAllContentLocallyBeforeStartingTaskSequence`.
If you specify `ClientsMediaAndPxe`, `MediaAndPxe`, or `MediaAndPxeHidden` for the **Availability** parameter, the default value for this parameter is `DownloadContentLocallyWhenNeededByRunningTaskSequence`.

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

### -DeployPurpose

Specify whether this deployment is available for users to install, or it's required to install at the deadline.

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

Specify a task sequence deployment object. To get this object, use the [Get-CMTaskSequenceDeployment](Get-CMTaskSequenceDeployment.md) cmdlet.

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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

If you create an alert for failed deployments, the site generates an alert when the percentage of failed deployments is higher than this number.

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

If you create an alert for successful deployments, the site generates an alert when the percentage of successful deployments is lower than this number.

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

Configure how the client handles the write filter on Windows Embedded devices.

- `$true`: Commit changes at the deadline or during a maintenance window. A restart is required.
- `$false`: Apply content on the overlay and commit later.

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

Specify whether the task sequence reruns on a computer if it previously ran before the scheduled mandatory time. By default, the task sequence always reruns.

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

Allow users to run the program independently of assignments.

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

Use this parameter to specify the deployment assignment, or _deadline_.

Use **AvailableDateTime** to specify when the deployment is _available_, and **DeadlineDateTime** to specify when the deployment _expires_.

Specify an array of schedule objects. A schedule object defines the mandatory assignment schedule for a deployment. To create a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

When the installation deadline is reached, set this parameter to `$true` to allow the task sequence to install outside the maintenance window.

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

When the installation deadline is reached, set this parameter to `$true` to allow system restart if necessary outside the maintenance window.

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

Specify the ID of the task sequence to deploy.

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

Indicates whether to allow clients on a metered internet connection to download content after the installation deadline, which might incur extra costs.

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
[Set-CMTaskSequenceDeployment](./Set-CMTaskSequenceDeployment.md)
[Remove-CMTaskSequenceDeployment](./Remove-CMTaskSequenceDeployment.md)

[Deploy a task sequence in Configuration Manager](/mem/configmgr/osd/deploy-use/deploy-a-task-sequence)
