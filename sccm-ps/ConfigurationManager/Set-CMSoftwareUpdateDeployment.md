---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Set-CMSoftwareUpdateDeployment
---

# Set-CMSoftwareUpdateDeployment

## SYNOPSIS

Modify a software update deployment.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMSoftwareUpdateDeployment [-AlertDateTime <DateTime>] [-AllowRestart <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-AvailableDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-Enable <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] -InputObject <IResultObject>
 [-NewDeploymentName <String>] [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>]
 [-ProtectedType <ProtectedType>] [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SendWakeupPacket <Boolean>] [-SoftDeadlineEnabled <Boolean>]
 [-SoftwareInstallation <Boolean>] [-TimeBasedOn <TimeType>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdateGroupDeploymentByIdMandatory
```
Set-CMSoftwareUpdateDeployment [-AlertDateTime <DateTime>] [-AllowRestart <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-AvailableDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-Enable <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-NewDeploymentName <String>]
 [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>]
 [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>]
 [-SendWakeupPacket <Boolean>] [-SoftDeadlineEnabled <Boolean>] [-SoftwareInstallation <Boolean>]
 -SoftwareUpdateGroupId <String> [-TimeBasedOn <TimeType>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdateGroupDeploymentByNameMandatory
```
Set-CMSoftwareUpdateDeployment [-AlertDateTime <DateTime>] [-AllowRestart <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-AvailableDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-Enable <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-NewDeploymentName <String>]
 [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>]
 [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>]
 [-SendWakeupPacket <Boolean>] [-SoftDeadlineEnabled <Boolean>] [-SoftwareInstallation <Boolean>]
 -SoftwareUpdateGroupName <String> [-TimeBasedOn <TimeType>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdateDeploymentByIdMandatory
```
Set-CMSoftwareUpdateDeployment [-AlertDateTime <DateTime>] [-AllowRestart <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-AvailableDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-Enable <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-NewDeploymentName <String>]
 [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>]
 [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>]
 [-SendWakeupPacket <Boolean>] [-SoftDeadlineEnabled <Boolean>] [-SoftwareInstallation <Boolean>]
 -SoftwareUpdateId <String> [-TimeBasedOn <TimeType>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdateDeploymentByNameMandatory
```
Set-CMSoftwareUpdateDeployment [-AlertDateTime <DateTime>] [-AllowRestart <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-AvailableDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-Enable <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-NewDeploymentName <String>]
 [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>]
 [-RequirePostRebootFullScan <Boolean>] [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>]
 [-SendWakeupPacket <Boolean>] [-SoftDeadlineEnabled <Boolean>] [-SoftwareInstallation <Boolean>]
 -SoftwareUpdateName <String> [-TimeBasedOn <TimeType>] [-UnprotectedType <UnprotectedType>]
 [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>] [-VerbosityLevel <VerbosityLevelType>]
 [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to modify a deployment of software updates in Configuration Manager.

For more information, see [Deploy software updates in Configuration Manager](/mem/configmgr/sum/deploy-use/deploy-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set a deployment with expiration time

This command sets a software update deployment by using a software update name and expiration time.

```powershell
Set-CMSoftwareUpdateDeployment -SoftwareUpdateName "CT" -DeploymentName "Contoso-test1" -NewDeploymentName "Contoso-test5" -Description "Contoso-test5-deployment" -CollectionName "All Mobile Devices" -SendWakeUpPacket $False -VerbosityLevel OnlySuccessAndErrorMessages -TimeBasedOn LocalTime -DeploymentAvailableDay 2013/11/24 -DeploymentAvailableTime 13:26 -DeploymentExpireDay 2014/7/22 -DeploymentExpireTime 4:30 -UserNotification DisplayAll -SoftwareInstallation $False -AllowRestart $False -RestartServer $False -RestartWorkstation $False -PersistOnWriteFilterDevice $True -GenerateSuccessAlert $False -PercentSuccess 99  -DisableOperationsManagerAlert $False -GenerateOperationsManagerAlert $False -ProtectedType NoInstall -UnprotectedType UnprotectedDistributionPoint -UseBranchCache $True -DownloadFromMicrosoftUpdate $False -AllowUseMeteredNetwork $False
```

### Example 2: Start a deployment without expiration time

This command sets a software update deployment by using a software update name but no specified expiration time.

```powershell
Set-CMSoftwareUpdateDeployment -SoftwareUpdateName "CT" -DeploymentName "Contoso-test2" -NewDeploymentName "Contoso-test6" -Description "Contoso-test6-deployment" -CollectionName "All Mobile Devices" -VerbosityLevel OnlyErrorMessages -TimeBasedOn LocalTime -DeploymentAvailableDay 2013/12/24 -DeploymentAvailableTime 3:56 -UserNotification DisplaySoftwareCenterOnly -PersistOnWriteFilterDevice $True -DisableOperationsManagerAlert $False -GenerateOperationsManagerAlert $False -ProtectedType NoInstall -UnprotectedType UnprotectedDistributionPoint -UseBranchCache $True -DownloadFromMicrosoftUpdate $False -AllowUseMeteredNetwork $False
```

### Example 3: Start a deployment by software update group name and expiration time

This command sets a software update deployment by using a software update group name and an expiration time.

```powershell
Set-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName "CTG" -DeploymentName "Contoso-test3" -NewDeploymentName "Contoso-test7" -Description "Contoso-test7-deployment" -CollectionName "All Mobile Devices" -SendWakeUpPacket $False -VerbosityLevel OnlySuccessAndErrorMessages -TimeBasedOn LocalTime -DeploymentAvailableDay 2013/11/24 -DeploymentAvailableTime 13:26 -DeploymentExpireDay 2014/7/22 -DeploymentExpireTime 4:30 -UserNotification DisplayAll -SoftwareInstallation $False -AllowRestart $False -RestartServer $False -RestartWorkstation $False -PersistOnWriteFilterDevice $True -GenerateSuccessAlert $False -PercentSuccess 99  -DisableOperationsManagerAlert $False -GenerateOperationsManagerAlert $False -ProtectedType NoInstall -UnprotectedType UnprotectedDistributionPoint -UseBranchCache $True -DownloadFromMicrosoftUpdate $False -AllowUseMeteredNetwork $False
```

### Example 4: Start a deployment by software update group name

This command starts a software update deployment by using a software update group name but no specified expiration time.

```powershell
Set-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName "CTG" -DeploymentName "Contoso-test4" -NewDeploymentName "Contoso-test8" -Description "Contoso-test8-deployment" -CollectionName "All Mobile Devices" -VerbosityLevel OnlyErrorMessages -TimeBasedOn LocalTime -DeploymentAvailableDay 2013/12/24 -DeploymentAvailableTime 3:56 -UserNotification DisplaySoftwareCenterOnly -PersistOnWriteFilterDevice $True -DisableOperationsManagerAlert $False -GenerateOperationsManagerAlert $False -ProtectedType NoInstall -UnprotectedType UnprotectedDistributionPoint -UseBranchCache $True -DownloadFromMicrosoftUpdate $False -AllowUseMeteredNetwork $False
```

## PARAMETERS

### -AlertDateTime

If **-GenerateSuccessAlert** is `$true`, specify a time to generate the alert.

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

### -AllowRestart

Indicates whether to allow a restart following installation.

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

### -AllowUseMeteredNetwork

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
Accept wildcard characters: True
```

### -DeploymentExpireDateTime

Specify an expiration time for the deployment.

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

### -DeploymentName

Specifies a name for a software update deployment in Configuration Manager.

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

Specifies a description for a software update deployment.

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

### -DownloadFromMicrosoftUpdate

Indicates whether clients download updates directly from Microsoft Update.

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

### -Enable

Indicates whether this deployment is enabled.

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

> [!IMPORTANT]
> This parameter currently only supports deployment of a single software update. It doesn't support deployment of software update groups.

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
Parameter Sets: SetByValueMandatory
Aliases: SoftwareUpdate, DeploymentSummary, SoftwareUpdateGroup, Assignment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NewDeploymentName

Rename this software update deployment.

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

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

Indicate whether to suppress a server restart, if a restart is required to complete update installation.

- `$true`: Suppress the restart
- `$false`: Allow servers to restart

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

Indicate whether to suppress a workstation restart, if a restart is required to complete update installation.

- `$true`: Suppress the restart
- `$false`: Allow servers to restart

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

### -SendWakeupPacket

Indicates whether to send a wake-up packet to computers before the deployment begins.

- `$True`: Configuration Manager wakes a computer from sleep.
- `$False`: It doesn't wake computers from sleep.

For computers to wake, first [configure wake on LAN](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

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

Set this parameter to `$true` to delay enforcement of this deployment according to user preferences, up to the grace period defined in client settings.

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

Indicates whether to allow the software update to install, even if the installation occurs outside of a maintenance window.

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

Specifies an ID for a software update group.
A software update group contains individual software updates.

```yaml
Type: String
Parameter Sets: SetSoftwareUpdateGroupDeploymentByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName

Specifies a name for a software update group.

```yaml
Type: String
Parameter Sets: SetSoftwareUpdateGroupDeploymentByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateId

Specifies an ID for a software update in Configuration Manager.

```yaml
Type: String
Parameter Sets: SetSoftwareUpdateDeploymentByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName

Specifies a name for a software update in Configuration Manager.

```yaml
Type: String
Parameter Sets: SetSoftwareUpdateDeploymentByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeBasedOn

Specifies that client computers use either local or UTC time to determine the availability of a program.
UTC time makes the software update available at the same time for all computers.

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

### System.Object

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdateDeployment](Get-CMSoftwareUpdateDeployment.md)

[New-CMSoftwareUpdateDeployment](New-CMSoftwareUpdateDeployment.md)

[Remove-CMSoftwareUpdateDeployment](Remove-CMSoftwareUpdateDeployment.md)

[Deploy software updates in Configuration Manager](/mem/configmgr/sum/deploy-use/deploy-software-updates)
