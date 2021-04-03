---
description: Create a software update deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: New-CMSoftwareUpdateDeployment
---

# New-CMSoftwareUpdateDeployment

## SYNOPSIS

Create a software update deployment.

## SYNTAX

### DeploySoftwareUpdateByValue (Default)
```
New-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-DeploymentName <String>]
 [-DeploymentType <DeploymentType>] [-Description <String>] [-DisableOperationsManagerAlert <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-GenerateSuccessAlert <Boolean>] -InputObject <IResultObject> [-PercentSuccess <Int32>]
 [-ProtectedType <ProtectedType>] [-DeployWithNoPackage <Boolean>] [-RequirePostRebootFullScan <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-SavedPackageId <String>]
 [-SoftDeadlineEnabled <Boolean>] [-SoftwareInstallation <Boolean>] [-TimeBasedOn <TimeType>]
 [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-DistributeCollectionName <String>] [-DistributeContent] [-DistributionPointGroupName <String>]
 [-DistributionPointName <String>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-DeadlineDateTime <DateTime>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeploySoftwareUpdateGroupById
```
New-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-DeploymentName <String>]
 [-DeploymentType <DeploymentType>] [-Description <String>] [-DisableOperationsManagerAlert <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-ProtectedType <ProtectedType>]
 [-DeployWithNoPackage <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SavedPackageId <String>] [-SoftDeadlineEnabled <Boolean>]
 [-SoftwareInstallation <Boolean>] -SoftwareUpdateGroupId <String> [-TimeBasedOn <TimeType>]
 [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-DistributeCollectionName <String>] [-DistributeContent] [-DistributionPointGroupName <String>]
 [-DistributionPointName <String>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-DeadlineDateTime <DateTime>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeploySoftwareUpdateGroupByName
```
New-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-DeploymentName <String>]
 [-DeploymentType <DeploymentType>] [-Description <String>] [-DisableOperationsManagerAlert <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-ProtectedType <ProtectedType>]
 [-DeployWithNoPackage <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SavedPackageId <String>] [-SoftDeadlineEnabled <Boolean>]
 [-SoftwareInstallation <Boolean>] -SoftwareUpdateGroupName <String> [-TimeBasedOn <TimeType>]
 [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-DistributeCollectionName <String>] [-DistributeContent] [-DistributionPointGroupName <String>]
 [-DistributionPointName <String>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-DeadlineDateTime <DateTime>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeploySoftwareUpdateById
```
New-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-DeploymentName <String>]
 [-DeploymentType <DeploymentType>] [-Description <String>] [-DisableOperationsManagerAlert <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-ProtectedType <ProtectedType>]
 [-DeployWithNoPackage <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SavedPackageId <String>] [-SoftDeadlineEnabled <Boolean>]
 [-SoftwareInstallation <Boolean>] -SoftwareUpdateId <String> [-TimeBasedOn <TimeType>]
 [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-DistributeCollectionName <String>] [-DistributeContent] [-DistributionPointGroupName <String>]
 [-DistributionPointName <String>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-DeadlineDateTime <DateTime>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeploySoftwareUpdateByName
```
New-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-DeploymentName <String>]
 [-DeploymentType <DeploymentType>] [-Description <String>] [-DisableOperationsManagerAlert <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-ProtectedType <ProtectedType>]
 [-DeployWithNoPackage <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SavedPackageId <String>] [-SoftDeadlineEnabled <Boolean>]
 [-SoftwareInstallation <Boolean>] -SoftwareUpdateName <String> [-TimeBasedOn <TimeType>]
 [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-DistributeCollectionName <String>] [-DistributeContent] [-DistributionPointGroupName <String>]
 [-DistributionPointName <String>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-DeadlineDateTime <DateTime>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to deploy software updates to a target collection.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
New-CMSoftwareUpdateDeployment -DeploymentName "updates deployment" -SoftwareUpdateGroupName "software update group" -CollectionName "Desktop clients for SUM" -Description "a more detailed description of this deployment" -DeploymentType Required -VerbosityLevel AllMessages -AvailableDateTime "2020/08/25 02:00AM" -DeadlineDateTime "2020/08/26 02:00AM" -UserNotification DisplaySoftwareCenterOnly -SoftwareInstallation $True  -AllowRestart $True  -RestartServer $False -RestartWorkstation $False -PersistOnWriteFilterDevice $True -RequirePostRebootFullScan $True -ProtectedType RemoteDistributionPoint
```

## PARAMETERS

### -AcceptEula

Some software updates include license terms. When you deploy software updates, the license terms aren't displayed. Add this parameter to automatically deploy all software updates regardless of an associated license term.

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

### -AllowRestart

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

### -AvailableDateTime

Specify when the software updates are available.

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

Specifies a collection object in Configuration Manager the deployment will target. Get this object with the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify the collection ID as the target for this software update deployment.

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

Specify the collection name as the target for this software update deployment.

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

Specify an optional description for the software update deployment.

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

Specify an installation deadline for required software updates. When the deadline is reached, the client installs required software updates on the device, and restarts the device if necessary. 

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

### -DeployWithNoPackage

Set this parameter to `$true` to not use a deployment package. Clients download software update content from peers or the Microsoft cloud.

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

### -DeploymentName

Specify a name for the software update deployment.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UpdateGroupDeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentType

Specify if this deployment is available for users to install or if it's a required installation at the specified deadline schedule.

```yaml
Type: DeploymentType
Parameter Sets: (All)
Aliases:
Accepted values: Required, Available

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description for the software update deployment.

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

### -DisableOperationsManagerAlert

Indicates whether to disable Operations Manager alerts during software updates.

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

Add this parameter to distribute the software update content when you create this deployment. Clients can't install the software updates until you distribute content to distribution points that the clients can access.

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

### -DownloadFromMicrosoftUpdate

If software update content isn't available on a distribution point in current, neighbor, or site boundary groups, download content from Microsoft Update.

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

### -GenerateOperationsManagerAlert

Indicates whether to generate Operations Manager alerts when a software installation fails.

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

### -GenerateSuccessAlert

If compliance of the deployment is below a specified threshold, the deployment generates an alert in the Configuration Manager console. The default threshold is 95 percent. To change the threshold, use the **PercentSuccess** parameter.

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

### -InputObject

Specify a software update object to deploy.

```yaml
Type: IResultObject
Parameter Sets: DeploySoftwareUpdateByValue
Aliases: SoftwareUpdate, SoftwareUpdateGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PercentSuccess

If you set **-GenerateSuccessAlert** to `$true`, use this parameter to specify the percentage compliance threshold at which the site generates a Configuration Manager console alert. If not specified, the site generates an alert if the deployment doesn't achieve 95 percent compliance by the specified deadline.

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

Indicates whether to install a software update on the temporary overlay and commit changes later, or commit the changes at an installation deadline or a maintenance window.

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

### -ProtectedType

Specify whether clients can use a distribution point from a neighbor boundary group or the default site boundary group.

```yaml
Type: ProtectedType
Parameter Sets: (All)
Aliases:
Accepted values: NoInstall, RemoteDistributionPoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequirePostRebootFullScan

This parameter controls the following console option: **Software updates deployment re-evaluation behavior upon restart**. If you set this option to `$true`, after clients restart when they install updates from this deployment, they then run a full update deployment evaluation cycle.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RunEvaluationAfterRestart

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestartServer

Indicates whether to allow a server to restart following a software update.

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

### -RestartWorkstation

Indicates whether to allow a workstation to restart following a software update.

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

### -SavedPackageId
```yaml
Type: String
Parameter Sets: (All)
Aliases: SavedDeploymentPackageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendWakeupPacket

Indicates whether to send a wake-up packet to computers before the deployment begins.

- `$True`: Configuration Manager wakes a computer from sleep.
- `$False`: It doesn't wake computers from sleep.

For computers to wake, first configure Wake On LAN.

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

### -SoftDeadlineEnabled
Starting in version 1906, use this parameter to set the following option on the **Deployment Schedule** page of the ADR deployment settings: **Delay enforcement of this deployment according to user preferences, up to the grace period defined in client settings**.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DelayEnforcementAndUpToGracePeriod

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInstallation

When the installation deadline is reached, set this parameter to `$true` to allow software update installation outside the maintenance window.

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

### -SoftwareUpdateGroupId

Specify the ID of a software update group to deploy.

```yaml
Type: String
Parameter Sets: DeploySoftwareUpdateGroupById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName

Specify the name of a software update group to deploy.

```yaml
Type: String
Parameter Sets: DeploySoftwareUpdateGroupByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateId

Specify the ID of a software update to deploy.

```yaml
Type: String
Parameter Sets: DeploySoftwareUpdateById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName

Specify the name of a software update to deploy.

```yaml
Type: String
Parameter Sets: DeploySoftwareUpdateByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeBasedOn

Specify that clients use either local or UTC time to determine the availability of the deployment. UTC time makes the software update available at the same time for all computers.

```yaml
Type: TimeType
Parameter Sets: (All)
Aliases:
Accepted values: LocalTime, Utc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeUnit

Specify the type of value of the **-TimeValue** parameter.

```yaml
Type: TimeUnitType
Parameter Sets: (All)
Aliases:
Accepted values: Hours, Days, Weeks, Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeValue

Specify an integer value for the time. Use the **-TimeUnit** parameter to determine the type of time for this value.

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

### -UnprotectedType

When software updates aren't available on any distribution points in current or neighbor boundary group, specify whether clients can download and install software updates from distribution points in the site default boundary group.

```yaml
Type: UnprotectedType
Parameter Sets: (All)
Aliases:
Accepted values: NoInstall, UnprotectedDistributionPoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseBranchCache

Indicates whether to use Windows BranchCache to download software update content.

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

### -UseMeteredNetwork

Indicates whether to allow clients to use a metered network to download updates.

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

### -UserNotification

Specify a user notification experience.

- `DisplayAll`: Display in Software Center and show all notifications
- `DisplaySoftwareCenterOnly`: Display in Software Center and only show notifications for computer restarts
- `HideAll`: Hide in Software Center and all notifications

```yaml
Type: UserNotificationType
Parameter Sets: (All)
Aliases:
Accepted values: DisplayAll, DisplaySoftwareCenterOnly, HideAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VerbosityLevel

Specify the state message detail level returned by clients for this software update deployment.

```yaml
Type: VerbosityLevelType
Parameter Sets: (All)
Aliases:
Accepted values: AllMessages, OnlySuccessAndErrorMessages, OnlyErrorMessages

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

### System.Object
## NOTES

## RELATED LINKS

[Set-CMSoftwareUpdateDeployment](Set-CMSoftwareUpdateDeployment.md)

[Start-CMSoftwareUpdateDeployment](Start-CMSoftwareUpdateDeployment.md)
