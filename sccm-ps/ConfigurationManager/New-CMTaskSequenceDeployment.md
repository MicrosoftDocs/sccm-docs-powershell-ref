---
description: Create a task sequence deployment
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/25/2020
schema: 2.0.0
title: New-CMTaskSequenceDeployment
---

# New-CMTaskSequenceDeployment

## SYNOPSIS

Create a task sequence deployment.

## SYNTAX

### SearchByValueMandatory (Default)
```
New-CMTaskSequenceDeployment [-AlertDateTime <DateTime>] [-AllowFallback <Boolean>]
 [-AllowSharedContent <Boolean>] [-Availability <MakeAvailableToType>] [-DeadlineDateTime <DateTime>]
 [-DeploymentOption <DeploymentOptionType>] [-DeployPurpose <DeployPurposeType>] [-InputObject] <IResultObject>
 [-InternetOption <Boolean>] [-PercentFailure <Int32>] [-PercentSuccess <Int32>]
 [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>]
 [-ScheduleEvent <ScheduleEventType[]>] [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-DistributeCollectionName <String>] [-DistributeContent] [-DistributionPointGroupName <String>]
 [-DistributionPointName <String>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
New-CMTaskSequenceDeployment [-AlertDateTime <DateTime>] [-AllowFallback <Boolean>]
 [-AllowSharedContent <Boolean>] [-Availability <MakeAvailableToType>] [-DeadlineDateTime <DateTime>]
 [-DeploymentOption <DeploymentOptionType>] [-DeployPurpose <DeployPurposeType>] [-InternetOption <Boolean>]
 [-PercentFailure <Int32>] [-PercentSuccess <Int32>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType[]>]
 [-ShowTaskSequenceProgress <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-TaskSequencePackageId] <String> [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-DistributeCollectionName <String>] [-DistributeContent] [-DistributionPointGroupName <String>]
 [-DistributionPointName <String>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMTaskSequenceDeployment** cmdlet creates a task sequence deployment. A task sequence deployment assigns a task sequence to a collection of computers.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Deploy a task sequence with many common parameters

This example does the following actions:

- Use the **Get-CMTaskSequence** cmdlet to get the task sequence object to deploy, and saves it in the **$DeployTS** variable
- Define the collection as the target of the deployment in the variable **$DeployCollection**
- Define the deployment available time at 8:00 PM on November 25, 2025, in the variable **$DeployAvailableTime**
- Define the deployment expiration time at 8:00 PM on January 25, 2026, in the variable **$DeployExpireTime**
- Define the deployment deadline at 8:00 PM on December 25, 2025, in the variable **$ScheduleDateTime**
- Use the **New-CMSchedule** cmdlet to create a schedule object for the deadline with a daily recurring schedule.
- Deploy the task sequence

```powershell
$DeployTS = Get-CMTaskSequence -TaskSequencePackageId 'PS104823'
$DeployCollection = 'PS11B7C4'
$DeployAvailableTime = [datetime]::ParseExact("20251125-200000", "yyyyMMdd-HHmmss", $null)
$DeployExpireTime = [datetime]::ParseExact("20260125-200000", "yyyyMMdd-HHmmss", $null)
$ScheduleDateTime = [datetime]::ParseExact("20251225-200000", "yyyyMMdd-HHmmss", $null)
$DeploySchedule = New-CMSchedule -DurationInterval Days -RecurInterval Days -RecurCount 1 -DurationCount 0 -Start $ScheduleDateTime
New-CMTaskSequenceDeployment -InputObject $DeployTS -DeployPurpose Required -AvailableDateTime $DeployAvailableTime -Availability Clients -RerunBehavior AlwaysRerunProgram -Schedule $DeploySchedule -CollectionId $DeployCollection -ShowTaskSequenceProgress $true -DeploymentOption DownloadAllContentLocallyBeforeStartingTaskSequence -RunFromSoftwareCenter $true -DeadlineDateTime $DeployExpireTime
```

## PARAMETERS

### -AlertDateTime

If you enable a deployment alert, use this parameter to specify a time for the alert.

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

Specify when this deployment is _available_.

Use **-DeadlineDateTime** to specify when the deployment _expires_, and **-Schedule** to specify the deployment assignment, or _deadline_.

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

Specify a collection object as the target for this task sequence deployment. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify a collection ID as the target for this task sequence deployment.

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

Specify a collection name as the target for this task sequence deployment.

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

### -DeadlineDateTime

Use this parameter to specify when the deployment _expires_.

Use **-AvailableDateTime** to specify when the deployment is _available_, and **-Schedule** to specify the deployment assignment, or _deadline_.

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

### -DeploymentOption

Specify how clients interact with the distribution points to get content for the task sequence. Not all options are available in specific scenarios. For more information, see [Deploy a task sequence - Deployment options](/mem/configmgr/osd/deploy-use/deploy-a-task-sequence#bkmk_deploy-options).

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

### -DistributeCollectionName

The site distributes content to the distribution point groups that are associated with this collection name.

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

Add this parameter to distribute the task sequence content when you create this deployment. Clients can't install the task sequence until you distribute content to distribution points that the clients can access.

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

The site distributes content to this distribution point group.

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

The site distributes content to this distribution point.

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

Specifies a task sequence object to deploy. To get a task sequence object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

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

Allow the task sequence to run for clients on the internet.

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

Use **-AvailableDateTime** to specify when the deployment is _available_, and **-DeadlineDateTime** to specify when the deployment _expires_.

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
Aliases: PackageId, TaskSequenceId

Required: True
Position: 0
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

### IResultObject#SMS_Advertisement

## NOTES

Make sure to use the schedule parameters appropriately:

- **-AvailableDateTime**: Specify when this deployment is _available_.

- **-DeadlineDateTime**: Specify when the deployment _expires_.

- **-Schedule**: Specify the deployment assignment, or _deadline_.

## RELATED LINKS

[Get-CMTaskSequenceDeployment](Get-CMTaskSequenceDeployment.md)
[Set-CMTaskSequenceDeployment](Set-CMTaskSequenceDeployment.md)
[Start-CMTaskSequenceDeployment](Start-CMTaskSequenceDeployment.md)
[Remove-CMTaskSequenceDeployment](Remove-CMTaskSequenceDeployment.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[Deploy a task sequence](/mem/configmgr/osd/deploy-use/deploy-a-task-sequence)
