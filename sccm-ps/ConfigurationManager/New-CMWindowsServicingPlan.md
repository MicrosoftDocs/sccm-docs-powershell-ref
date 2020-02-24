---
author: aczechowski
description: Creates a Windows 10 servicing plan.
external help file: AdminUI.PS.Sum-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMWindowsServicingPlan
titleSuffix: Configuration Manager
---

# New-CMWindowsServicingPlan

## SYNOPSIS
Creates a Windows 10 servicing plan.

## SYNTAX

### NewByCollectionName
```
New-CMWindowsServicingPlan -Name <String> [-Description <String>] -CollectionName <String> [-Enable <Boolean>]
 [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>] [-Language <String[]>] [-Required <String[]>]
 [-Title <String[]>] [-RunType <RunType>] [-Schedule <IResultObject>] [-UseUtc <Boolean>]
 [-AvailableTime <Int32>] [-AvailableImmediately <Boolean>] [-AvailableTimeUnit <TimeUnitType>]
 [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>] [-DeadlineTimeUnit <TimeUnitType>]
 [-UserNotification <UserNotificationType>] [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>]
 [-AllowRestart <Boolean>] [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>]
 [-WriteFilterHandling <Boolean>] [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>]
 [-AlertTime <Int32>] [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-DeploymentPackage <IResultObject>] [-DownloadFromInternet <Boolean>] [-Location <String>]
 [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>] [-LanguageSelection <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewByCollection
```
New-CMWindowsServicingPlan -Name <String> [-Description <String>] -Collection <IResultObject>
 [-Enable <Boolean>] [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>] [-Language <String[]>]
 [-Required <String[]>] [-Title <String[]>] [-RunType <RunType>] [-Schedule <IResultObject>]
 [-UseUtc <Boolean>] [-AvailableTime <Int32>] [-AvailableImmediately <Boolean>]
 [-AvailableTimeUnit <TimeUnitType>] [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>]
 [-DeadlineTimeUnit <TimeUnitType>] [-UserNotification <UserNotificationType>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowRestart <Boolean>]
 [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>] [-WriteFilterHandling <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>] [-AlertTime <Int32>]
 [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-DeploymentPackage <IResultObject>] [-DownloadFromInternet <Boolean>] [-Location <String>]
 [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>] [-LanguageSelection <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewByCollectionId
```
New-CMWindowsServicingPlan -Name <String> [-Description <String>] -CollectionId <String> [-Enable <Boolean>]
 [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>] [-Language <String[]>] [-Required <String[]>]
 [-Title <String[]>] [-RunType <RunType>] [-Schedule <IResultObject>] [-UseUtc <Boolean>]
 [-AvailableTime <Int32>] [-AvailableImmediately <Boolean>] [-AvailableTimeUnit <TimeUnitType>]
 [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>] [-DeadlineTimeUnit <TimeUnitType>]
 [-UserNotification <UserNotificationType>] [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>]
 [-AllowRestart <Boolean>] [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>]
 [-WriteFilterHandling <Boolean>] [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>]
 [-AlertTime <Int32>] [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-DeploymentPackage <IResultObject>] [-DownloadFromInternet <Boolean>] [-Location <String>]
 [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>] [-LanguageSelection <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMWindowsServicingPlan** cmdlet creates a Windows 10 servicing plan.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a servicing plan by collection ID
```
PS XYZ:\> $Lang = ("Japanese", "English", "French")
PS XYZ:\> $Required = (">=1", "<=100")
PS XYZ:\> $Title = ("Title1", "Title2", "Title3")
PS XYZ:\> New-CMWindowsServicingPlan -Name "Test01" -CollectionId MP40001A -Description "Servicing Plan description01" -SendWakeupPacket $False -VerboseLevel AllMessages -Language $Lang -Required $Required -Title $Title -RunType DoNotRunThisRuleAutomatically -UseUtc $True -AvailableImmediately $True -DeadlineImmediately $False -UserNotification DisplayAll -AllowSoftwareInstallationOutsideMaintenanceWindow $True -AllowRestart $True -SuppressRestartServer $True -SuppressRestartWorkstation $True -DeploymentPackage (Get-CMSoftwareUpdateDeploymentPackage -Name "SUDP01")
```

The first command creates a list of languages and stores the list in the $Lang variable.

The second command creates a list of search strings and stores the list in the $Required variable.
This search string will find software updates required on at least one computer and maximum of 100 computers.

The third command creates a list of software update titles and stores the list in the $Title variable.

The last command gets the software update deployment package named SUDP01 and then creates a Windows servicing plan named Test for the target collection with the ID MP40001A.
The command adds the upgrade filter languages stored in $Lang, the required filter stored in $Required, and the software update title filter stored in $Title.

### Example 2: Create a servicing plan by collection name
```
PS XYZ:\> $LangSelect = ("Japanese", "English", "French", "German")
PS XYZ:\> New-CMWindowsServicingPlan -Name "Test02" -CollectionName "ColName02" -DeploymentPackage (Get-CMSoftwareUpdateDeploymentPackage -Name "SUP02") -WriteFilterHandling $True -GenerateSuccessAlert $True -SuccessPercentage $True -AlertTime 10 -AlertTimeUnit Days -DisableOperationManager $True -GenerateOperationManagerAlert $True -NoInstallOnRemote $True -NoInstallOnUnprotected $True -UseBranchCache $True -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True -DownloadFromInternet $True -Location "\\TestSevr\WSUSTemp" -DeploymentRing Cbb -UpdateDeploymentWaitDay 20 -LanguageSelection $LangSelect
```

The first command creates a list of language selection languages and stores the list in the $LangSelect variable.

The second command gets the software update deployment package named SUP02 and then creates a Windows servicing plan named Test02 for the target collection named ColName02.
The command adds the language select languages stored in $LangSelect.

## PARAMETERS

### -AlertTime
Specifies an integer offset from an update deployment deadline.
The rule uses this value to specify when the rule generates alerts.
Specify a time unit by using the *AlertTimeUnit* parameter.

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

### -AlertTimeUnit
Specifies a unit of time for the *AlertTime* parameter.
Valid values are:

- Hours
- Days
- Weeks
- Months

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

### -AllowRestart
Indicates whether a system restart is allowed to be performed outside of any defined maintenance windows when the installation deadline is reached.

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

### -AllowSoftwareInstallationOutsideMaintenanceWindow
Indicates whether software installation is allowed to be performed outside of any defined maintenance windows when the installation deadline is reached.

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

### -AvailableImmediately
Indicates whether software updates are available to install as soon as possible after the rule is run.

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

### -AvailableTime
Specify when software updates are available.

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

### -AvailableTimeUnit
Specifies the time unit type for the software available time.
Valid values are:

- Hours
- Days
- Weeks
- Months

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

### -Collection
Specifies the target device collection object to be used for the servicing plan.
To obtain a device collection object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: NewByCollection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of the target device collection to be used for the servicing plan.

```yaml
Type: String
Parameter Sets: NewByCollectionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of the target device collection to be used for the servicing plan.

```yaml
Type: String
Parameter Sets: NewByCollectionName
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

### -DeadlineImmediately
Indicates whether required software updates are installed as soon as possible when the deadline is reached.

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

### -DeadlineTime
Specifies the number of time units for the deadline.

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

### -DeadlineTimeUnit
Specifies the time unit type for the deadline.
Valid values are:

- Hours
- Days
- Weeks
- Months

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

### -DeploymentPackage
Specifies a software update deployment package.
To obtain a software update deployment package, use the [Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentRing
Specifies the Windows readiness state to which the servicing plan should apply.
Valid values are:

- CB
- Release
- BusinessMainstream
- Cbb
- Ltsb

```yaml
Type: DeploymentRing
Parameter Sets: (All)
Aliases:
Accepted values: CB, Release, BusinessMainstream, Cbb, Ltsb

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the servicing plan.

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

### -DisableOperationManager
Indicates whether to disable System Center Operations Manager alerts during software updates.

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

### -DownloadFromInternet
Indicates whether to download software updates from the Internet.

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

### -DownloadFromMicrosoftUpdate
Indicates whether computers download content from Microsoft Update if the software updates are unavailable on a preferred distribution point or remote distribution point.

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
Indicates whether the servicing plan is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Enabled, EnableDeployment

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GenerateOperationManagerAlert
Indicates whether to generate Operations Manager alerts during a software update.

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
Indicates whether to generate an alert for successful deployment.

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

### -Language
Specifies an array of languages used to filter software upgrades that will be added to the service plan.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LanguageSelection
Specifies an array of languages, as strings.
Computers download software updates available in the specified languages, in addition to non-language-specific updates.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Specifies a network location to where the downloaded updates are located.

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

### -Name
Specifies a name for the servicing plan.
The name must be unique, help to describe the objective of the rule, and identify it from others in the Configuration Manager site.

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

### -NoInstallOnRemote
Indicates whether to allow installation of updates on remote systems.
If you specify a value of $True, if the client is within a slow or unreliable network boundary, or when the client uses a fallback source location for content, then Configuration Manager does not install software updates.
If you specify a value of $False, installation proceeds.

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

### -NoInstallOnUnprotected
Indicates whether to allow installation of updates on unprotected systems.
If you specify a value of $True, if software updates are not available on any preferred distribution points, Configuration Manager does not download and install software updates.
If you specify a value of $False, installation proceeds.

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

### -Required
Specifies an array of search strings used to filter software upgrades that will be added to the service plan.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunType
Specifies the mode in which an update runs.
Valid values are:

- DoNotRunThisRuleAutomatically
- RunTheRuleAfterAnySoftwareUpdatePointSynchronization
- RunTheRuleOnSchedule

```yaml
Type: RunType
Parameter Sets: (All)
Aliases:
Accepted values: DoNotRunThisRuleAutomatically, RunTheRuleAfterAnySoftwareUpdatePointSynchronization, RunTheRuleOnSchedule

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies the deadline time (from deployment available time).
To create a schedule, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -SendWakeupPacket
Indicates whether to send a wake-up packet to computers before the deployment begins.
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

### -SuccessPercentage
Specifies a percentage for client compliance as an integer from 0 to 99.
If compliance falls below this percentage, Configuration Manager produces optional alerts.

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

### -SuppressRestartServer
Indicates whether a system restart is suppressed on servers when a software update requires a system restart to complete the installation process.

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

### -SuppressRestartWorkstation
Indicates whether a system restart is suppressed on workstations when a software update requires a system restart to complete the installation process.

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

### -Title
Specifies an array of search strings used to filter software update titles that will be added to the service plan.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateDeploymentWaitDay
Specifies the number of days to wait after Microsoft has published a new upgrade before deploying in your environment.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: UpdateDeploymentWaitDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseBranchCache
Indicates whether to use a branch cache.
If you specify a value of $True, clients share content on the same subnet.

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
Indicates whether the schedule for this deployment is evaluated based upon Universal Coordinated Time (UTC).

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
Specifies the notification behavior of the user visual experience.
Valid values are:

- DisplayAll
- DisplaySoftwareCenterOnly
- HideAll

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

### -VerboseLevel
Specifies the level of detail you want clients to report for deployments that this rule creates.
Valid values are:

- AllMessages
- OnlyErrorMessages
- OnlySuccessAndErrorMessages

```yaml
Type: VerboseLevelType
Parameter Sets: (All)
Aliases:
Accepted values: OnlyErrorMessages, OnlySuccessAndErrorMessages, AllMessages

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

### -WriteFilterHandling
Indicates whether changes are committed at deadline or during a maintenance window (requires restarts).
If set to $False, content is applied on the overlay and committed later.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)

[Get-CMWindowsServicingPlan](Get-CMWindowsServicingPlan.md)
