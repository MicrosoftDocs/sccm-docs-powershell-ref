---
description: Initiates a software update deployment in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Start-CMSoftwareUpdateDeployment
---

# Start-CMSoftwareUpdateDeployment

## SYNOPSIS
(Deprecated) Initiates a software update deployment in Configuration Manager.

## SYNTAX

### DeploySoftwareUpdateByValue (Default)
```
Start-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 -CollectionName <String> [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-EnforcementDeadline <DateTime>] [-EnforcementDeadlineDay <DateTime>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] -InputObject <IResultObject>
 [-PercentSuccess <Int32>] [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-SendWakeupPacket <Boolean>]
 [-SoftwareInstallation <Boolean>] [-TimeBasedOn <TimeType>] [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>]
 [-VerbosityLevel <VerbosityLevelType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateByName
```
Start-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 -CollectionName <String> [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-EnforcementDeadline <DateTime>] [-EnforcementDeadlineDay <DateTime>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>]
 [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SendWakeupPacket <Boolean>] [-SoftwareInstallation <Boolean>]
 -SoftwareUpdateName <String> [-TimeBasedOn <TimeType>] [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>]
 [-VerbosityLevel <VerbosityLevelType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateById
```
Start-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 -CollectionName <String> [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-EnforcementDeadline <DateTime>] [-EnforcementDeadlineDay <DateTime>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>]
 [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SendWakeupPacket <Boolean>] [-SoftwareInstallation <Boolean>]
 -SoftwareUpdateId <String> [-TimeBasedOn <TimeType>] [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>]
 [-VerbosityLevel <VerbosityLevelType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateGroupByName
```
Start-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 -CollectionName <String> [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-EnforcementDeadline <DateTime>] [-EnforcementDeadlineDay <DateTime>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>]
 [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SendWakeupPacket <Boolean>] [-SoftwareInstallation <Boolean>]
 -SoftwareUpdateGroupName <String> [-TimeBasedOn <TimeType>] [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>]
 [-VerbosityLevel <VerbosityLevelType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateGroupById
```
Start-CMSoftwareUpdateDeployment [-AcceptEula] [-AllowRestart <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 -CollectionName <String> [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-DeploymentName <String>] [-DeploymentType <DeploymentType>] [-Description <String>]
 [-DisableOperationsManagerAlert <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-EnforcementDeadline <DateTime>] [-EnforcementDeadlineDay <DateTime>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>]
 [-PersistOnWriteFilterDevice <Boolean>] [-ProtectedType <ProtectedType>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-SendWakeupPacket <Boolean>] [-SoftwareInstallation <Boolean>]
 -SoftwareUpdateGroupId <String> [-TimeBasedOn <TimeType>] [-TimeUnit <TimeUnitType>] [-TimeValue <Int32>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-UserNotification <UserNotificationType>]
 [-VerbosityLevel <VerbosityLevelType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!IMPORTANT]
> This cmdlet is deprecated. Use [New-CMSoftwareUpdateDeployment](New-CMSoftwareUpdateDeployment.md) instead.

The **Start-CMSoftwareUpdateDeployment** cmdlet initiates a software update deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Start a required deployment by software update name
```
PS XYZ:\> Start-CMSoftwareUpdateDeployment -SoftwareUpdateName "CT" -CollectionName "All Systems" -DeploymentName "Contoso-test" -Description "Contoso-test-deployment" -DeploymentType Required -SendWakeUpPacket $True -VerbosityLevel AllMessages -TimeBasedOn UTC -DeploymentAvailableDay 2012/10/24 -DeploymentAvailableTime 23:56 -DeploymentExpireDay 2013/10/21 -DeploymentExpireTime 11:20 -UserNotification HideAll -SoftwareInstallation $True -AllowRestart $True -RestartServer $True -RestartWorkstation $True -PersistOnWriteFilterDevice $False -GenerateSuccessAlert $True -PercentSuccess 90 -TimeValue 10 -TimeUnit Days -DisableOperationsManagerAlert $True -GenerateOperationsManagerAlert $True -ProtectedType RemoteDistributionPoint -UnprotectedType NoInstall -UseBranchCache $False -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True
```

This command starts a required software update deployment by using a software update name.

### Example 2: Start an available deployment by software update name
```
PS XYZ:\> Start-CMSoftwareUpdateDeployment -SoftwareUpdateName "CT" -CollectionName "All Systems" -DeploymentName "Contoso-test2" -Description "Contoso-test2-deployment" -DeploymentType Available -VerbosityLevel AllMessages -TimeBasedOn UTC -DeploymentAvailableDay 2012/10/24 -DeploymentAvailableTime 23:56 -UserNotification DisplayAll -PersistOnWriteFilterDevice $False -DisableOperationsManagerAlert $True -GenerateOperationsManagerAlert $True -ProtectedType RemoteDistributionPoint -UnprotectedType NoInstall -UseBranchCache $False -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True
```

This command starts an available software update deployment by using a software update name.

### Example 3: Start a required deployment by software update group name
```
PS XYZ:\> Start-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName "CTG" -CollectionName "All Systems" -DeploymentName "Contoso-test3" -Description "Contoso-test3-deployment" -DeploymentType Required -SendWakeUpPacket $True -VerbosityLevel AllMessages -TimeBasedOn UTC -DeploymentAvailableDay 2012/10/24 -DeploymentAvailableTime 23:56 -DeploymentExpireDay 2013/10/21 -DeploymentExpireTime 11:20 -UserNotification HideAll -SoftwareInstallation $True -AllowRestart $True -RestartServer $True -RestartWorkstation $True -PersistOnWriteFilterDevice $False -GenerateSuccessAlert $True -PercentSuccess 90 -TimeValue 10 -TimeUnit Days -DisableOperationsManagerAlert $True -GenerateOperationsManagerAlert $True -ProtectedType RemoteDistributionPoint -UnprotectedType NoInstall -UseBranchCache $False -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True
```

This command starts a software update deployment by using a collection name and an input object.

### Example 4: Start a deployment by software update group name
```
PS XYZ:\> Start-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName "CTG" -CollectionName "All Systems" -DeploymentName "Contoso-test4" -Description "Contoso-test4-deployment" -DeploymentType Available -VerbosityLevel AllMessages -TimeBasedOn UTC -DeploymentAvailableDay 2012/10/24 -DeploymentAvailableTime 23:56 -UserNotification DisplayAll -PersistOnWriteFilterDevice $False -DisableOperationsManagerAlert $True -GenerateOperationsManagerAlert $True -ProtectedType RemoteDistributionPoint -UnprotectedType NoInstall -UseBranchCache $False -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True
```

This command starts a software update deployment by using a software update group name.

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

### -CollectionName
Specifies a name of a collection in Configuration Manager.
A collection is a group of client computers.

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

### -DeploymentAvailableDay
Specifies a day, in MM/DD/YYYY format, when a software update deployment is available.
By default, the update is available immediately.

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
Specifies a time, in HH:MM format, when a software update deployment is available.
By default, the update is available immediately.

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
Specifies a deployment type in Configuration Manager.

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
Indicates whether to disable System Center 2012 - Operations Manager alerts during software updates.

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

### -EnforcementDeadline
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: DeploymentExpireTime

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnforcementDeadlineDay
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: DeploymentExpireDay

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
Indicates whether to generate alerts when a software installation succeeds.

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
Specifies a percent success.

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
Specifies a protected type.

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

### -RestartServer
Indicates whether to allow a server to restart following a software update.
Setting this value to $True prevents the server from restarting.
Setting this value to $False allows the server to restart.

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
Setting this value to $True prevents the computer from restarting.
Setting this value to $False allows the computer to restart.

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
Parameter Sets: DeploySoftwareUpdateGroupById
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
Parameter Sets: DeploySoftwareUpdateGroupByName
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
Parameter Sets: DeploySoftwareUpdateById
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
Parameter Sets: DeploySoftwareUpdateByName
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

### -TimeUnit
Specifies the time unit in Configuration Manager.
Valid values are:

- Days
- Hours
- Months
- Weeks

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
Specifies a time value in the units specified in the *TimeUnit* parameter.

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
Specifies an unprotected type.

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
Indicates whether to use Branch Cache as a distribution point for updates.

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
Specifies a user notification type.

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
Specifies verbosity level.
Valid values are:

- AllMessages
- OnlyErrorMessages
- OnlySuccessAndErrorMessages

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

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdateDeployment](Set-CMSoftwareUpdateDeployment.md)
