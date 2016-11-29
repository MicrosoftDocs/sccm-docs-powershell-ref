---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834066
schema: 2.0.0
ms.assetid: 9156F844-66C1-4144-9716-8F5E549923CD
---

# Set-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Modifies Configuration Manager deployment rules for automatic software updates.

## SYNTAX

### SearchByNameMandatory (Default)
```
Set-CMSoftwareUpdateAutoDeploymentRule -Name <String> [-NewName <String>] [-Description <String>]
 [-CollectionName <String>] [-AddToExistingSoftwareUpdateGroup <Boolean>] [-EnabledAfterCreate <Boolean>]
 [-Enable <Boolean>] [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>]
 [-DeployWithoutLicense <Boolean>] [-RunType <RunType>] [-Schedule <IResultObject>] [-UseUtc <Boolean>]
 [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>]
 [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>] [-DeadlineTimeUnit <TimeUnitType>]
 [-UserNotification <UserNotificationType>] [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>]
 [-AllowRestart <Boolean>] [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>]
 [-WriteFilterHandling <Boolean>] [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>]
 [-AlertTime <Int32>] [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-LanguageSelection <String[]>] [-ArticleId <String[]>] [-BulletinId <String[]>]
 [-CustomSeverity <SeverityType[]>] [-DateReleasedOrRevised <DateReleasedOrRevisedType>]
 [-UpdateDescription <String[]>] [-DownloadFromInternet <Boolean>] [-Location <String>] [-Language <String[]>]
 [-Required <String[]>] [-Severity <SeverityType[]>] [-Superseded <Boolean>] [-Title <String[]>]
 [-UpdateClassification <String[]>] [-Product <String[]>] [-MicrosoftAsVendor <Boolean>] [-Force] [-PassThru]
 [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMSoftwareUpdateAutoDeploymentRule -Id <String[]> [-NewName <String>] [-Description <String>]
 [-CollectionName <String>] [-AddToExistingSoftwareUpdateGroup <Boolean>] [-EnabledAfterCreate <Boolean>]
 [-Enable <Boolean>] [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>]
 [-DeployWithoutLicense <Boolean>] [-RunType <RunType>] [-Schedule <IResultObject>] [-UseUtc <Boolean>]
 [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>]
 [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>] [-DeadlineTimeUnit <TimeUnitType>]
 [-UserNotification <UserNotificationType>] [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>]
 [-AllowRestart <Boolean>] [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>]
 [-WriteFilterHandling <Boolean>] [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>]
 [-AlertTime <Int32>] [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-LanguageSelection <String[]>] [-ArticleId <String[]>] [-BulletinId <String[]>]
 [-CustomSeverity <SeverityType[]>] [-DateReleasedOrRevised <DateReleasedOrRevisedType>]
 [-UpdateDescription <String[]>] [-DownloadFromInternet <Boolean>] [-Location <String>] [-Language <String[]>]
 [-Required <String[]>] [-Severity <SeverityType[]>] [-Superseded <Boolean>] [-Title <String[]>]
 [-UpdateClassification <String[]>] [-Product <String[]>] [-MicrosoftAsVendor <Boolean>] [-Force] [-PassThru]
 [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMSoftwareUpdateAutoDeploymentRule -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-CollectionName <String>] [-AddToExistingSoftwareUpdateGroup <Boolean>] [-EnabledAfterCreate <Boolean>]
 [-Enable <Boolean>] [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>]
 [-DeployWithoutLicense <Boolean>] [-RunType <RunType>] [-Schedule <IResultObject>] [-UseUtc <Boolean>]
 [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>]
 [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>] [-DeadlineTimeUnit <TimeUnitType>]
 [-UserNotification <UserNotificationType>] [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>]
 [-AllowRestart <Boolean>] [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>]
 [-WriteFilterHandling <Boolean>] [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>]
 [-AlertTime <Int32>] [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-LanguageSelection <String[]>] [-ArticleId <String[]>] [-BulletinId <String[]>]
 [-CustomSeverity <SeverityType[]>] [-DateReleasedOrRevised <DateReleasedOrRevisedType>]
 [-UpdateDescription <String[]>] [-DownloadFromInternet <Boolean>] [-Location <String>] [-Language <String[]>]
 [-Required <String[]>] [-Severity <SeverityType[]>] [-Superseded <Boolean>] [-Title <String[]>]
 [-UpdateClassification <String[]>] [-Product <String[]>] [-MicrosoftAsVendor <Boolean>] [-Force] [-PassThru]
 [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdateAutoDeploymentRule** cmdlet modifies Microsoft System Center Configuration Manager deployment rules for automatic software updates.
To create a rule, use the Get-CMSoftwareUpdateAutoDeploymentRule cmdlet.

System Center Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, System Center Configuration Manager adds updates that qualify for the rule to a software update group.
The System Center Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

## EXAMPLES

### Example 1: Modify the language selection and name of a rule
```
PS C:\>Set-CMSoftwareUpdateAutoDeploymentRule -Name "DeploymentRule07" -NewName "DeploymentRule07Revised" -Description "Update rule to use Portuguese (Brazil)." -LanguageSelection "Portuguese (Brazil)"
```

This command modifies the automatic deployment rule named DeploymentRule07.
The command specifies Portuguese (Brazil) as the language selection.
The command also changes the name of the rule to DeploymentRule07Revised.

## PARAMETERS

### -AddToExistingSoftwareUpdateGroup
Indicates whether the rule adds to an existing update group.
If this value is $True, each time the rule runs and finds new updates, it adds them to an existing update group.
If this value is $False, it creates a new update group.
Specify the existing update group or assign a name for the new update group by using the *DeploymentPackageName* parameter.

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
The acceptable values for this parameter are:

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

### -AllowRestart
Indicates whether to allow a computer to restart if the update deployment takes place outside of a maintenance window.
A maintenance window is a specified period of time used for computer maintenance and updates.
If this value is $True, this Configuration Manager restarts the computer, if necessary to complete the update.
If this value is $False, Configuration Manager does not restart the computer.

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
Indicates whether the update deployment takes place even if scheduled outside of a maintenance window.
A maintenance window is a specified period of time used for computer maintenance and updates.
If this value is $True, this Configuration Manager deploys the update even the scheduled time falls outside the service window.
If this value is $False, Configuration Manager does not deploy the update outside the service window, but Configuration Manager waits until it can deploy in a service window.

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

### -ArticleId
Specifies an array of criteria, as strings, for software updates.
The rule adds software updates that have article IDs that meet specified criteria to the software update group.

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

### -AvailableImmediately
Indicates whether this rule deploys updates as soon as the updates become available.
If you specify a value of $False, use the *AvailableTime* and *AvailableTimeUnit* parameters to specify how long after the rule runs to deploy the updates.

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
Specifies a period of time as an integer.
Configuration Manager deploys the updates this long after the rule runs.
Specify a time unit by using the *AvailableTimeUnit* parameter.

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
Specifies a unit of time for the *AvailableTime* parameter.
The acceptable values for this parameter are:

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

### -BulletinId
Specifies an array of criteria, as strings, for software updates.
The rule adds software updates that have bulletin IDs that meet specified criteria to the software update group.

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

### -CollectionName
Specifies the name of device collection or user collection.

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

### -CustomSeverity
Specifies an array of custom severity types for software updates.
The rule adds software updates that have custom severity levels that meet specified criteria to the software update group.
The acceptable values for this parameter are:

- Critical
- Important
- Low
- Moderate
- None

```yaml
Type: SeverityType[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Low, Moderate, Important, Critical

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DateReleasedOrRevised
Specifies a date released or revised for software updates.
The rule adds software updates that have a date that meets specified criteria to the software update group.
The acceptable values for this parameter are:

- Last10months
- Last11months
- Last12hours
- Last14days
- Last16hours
- Last1day
- Last1hour
- Last1month
- Last1year
- Last20hours
- Last21days
- Last28days
- Last2days
- Last2hours
- Last2months
- Last3days
- Last3hours
- Last3months
- Last4days
- Last4hours
- Last4months
- Last5days
- Last5months
- Last6days
- Last6months
- Last7days
- Last7months
- Last8hours
- Last8months
- Last9months

```yaml
Type: DateReleasedOrRevisedType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Last1Hour, LastHour, Last2Hours, Last3Hours, Last4Hours, Last8Hours, Last12Hours, Last16Hours, Last20Hours, Last1Day, LastDay, Last2Days, Last3Days, Last4Days, Last5Days, Last6Days, Last7Days, Last14Days, Last21Days, Last28Days, LastMonth, Last1Month, Last2Months, Last3Months, Last4Months, Last5Months, Last6Months, Last7Months, Last8Months, Last9Months, Last10Months, Last11Months, Last1Year, LastYear, Last12Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeadlineImmediately
Indicates whether to impose the deadline as soon as the rule runs.
If you specify a value of $False, use the *DeadlineTime* and *DeadlineTimeUnit* parameters to specify how long after the rule runs to set the deadline.
After the deadline, Configuration Manager installs required updates.

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
Specifies a period of time as an integer.
The deadline for updates is this long after the rule runs.
Specify a time unit by using the *DeadlineTimeUnit* parameter.

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
Specifies a unit of time for the *DeadlineTime* parameter.
The acceptable values for this parameter are:

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

### -DeployWithoutLicense
Indicates whether the rule deploys updates without licenses.
If you specify a value of $True, Configuration Manager deploys all updates for this rule and approves any license agreements.
If this value is $False, Configuration Manager deploys only updates that do not include a license or for which the license agreement has been approved.

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

### -DeploymentRing


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
Specifies a description for the automatic deployment rule for software updates.

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
Indicates whether to disable System Center 2016 - Operations Manager alerts during software updates.

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

### -DownloadFromInternet


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
Indicates whether computers download content from Microsoft Update if that content is unavailable on a preferred distribution point of remote distribution point.

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

### -EnabledAfterCreate
Indicates whether to enable software deployment for the associated software update group after this rule runs.
If this value is $False, deploy the software update group manually.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableAfterCreate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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

### -Id
Specifies an array of IDs of automatic deployment rules for software updates.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an object representing an automatic deployment rule for software updates.
To obtain an object representing a rule, use **Get-CMSoftwareUpdateAutoDeploymentRule**.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Language
Specifies an array of criteria, as strings, for software updates.
The rule adds software updates that have languages that meet specified criteria to the software update group.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Languages, UpdateLocales, UpdateLocale

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

### -MicrosoftAsVendor
Indicates whether the rule includes only updates that have Microsoft as the vendor.

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

### -Name
Specifies a name for the automatic deployment rule for software updates.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the automatic deployment rule for software updates.

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

### -NoInstallOnRemote
Indicates whether to disallow installation of updates on remote systems.
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
Indicates whether to disallow installation of updates on unprotected systems.
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

### -PassThru


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

### -Product
Specifies an array of criteria, as strings, for software updates.
The rule adds software updates for products that meet specified criteria to the software update group.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Products

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Required
Specifies an array of criteria, as strings, for software updates.
The rule adds software updates identified by required that meet specified criteria to the software update group.

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
Specifies the mode in which an update runs on the client computer.
The acceptable values for this parameter are:

- DoNotRunThisRuleAutomatically
- RunTheRuleAfterAnySoftwareUpdatePointSynchronization
- RunTheRuleOnSchedule

If you specify RunTheRuleOnSchedule, specify a schedule by using the *Schedule* parameter.

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
Specifies a schedule object for the deployment.
To obtain a schedule object, use the New-CMSchedule cmdlet.
Specify a schedule for this parameter if you specify a value of RunTheRuleOnSchedule for the *RunType* parameter.

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

### -Severity
Specifies an array of severity levels for software updates.
The rule adds software updates for specified severity types to the software update group.
The acceptable values for this parameter are:

- Critical
- Important
- Low
- Moderate
- None

```yaml
Type: SeverityType[]
Parameter Sets: (All)
Aliases: Severities
Accepted values: None, Low, Moderate, Important, Critical

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

### -Superseded
Indicates whether the rule adds updates superseded by other updates.

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

### -SuppressRestartServer
Indicates whether to suppress a required update for a server.
Some software updates require a system restart to complete the installation process.

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
Indicates whether to suppress a required update for a workstation.
Some software updates require a system restart to complete the installation process.

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
Specifies an array of criteria, as strings, for software updates.
The rule adds software updates that have titles that meet specified criteria to the software update group.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Titles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateClassification
Specifies an array of criteria, as strings, for software updates.
The rule adds software updates that have update classifications that meet specified criteria to the software update group.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: UpdateClassifications

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateDeploymentWaitDay


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

### -UpdateDescription
Specifies an array of criteria, as strings, for software updates.
The rule adds software updates that have update descriptions that meet specified criteria to the software update group.

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

### -UseBranchCache
Indicates whether to use a branch cache for this update deployment.
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
Indicates whether to use Coordinated Universal Time (UTC), also known as Greenwich Mean Time.
If this value is $True, Configuration Manager uses UTC for this deployment.
If this value is $False, Configuration Manager uses local time.

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
Specifies the type of user notification.
The acceptable values for this parameter are:

- DisplayAll.
Display in Software Center and show all notifications.
- DisplaySoftwareCenterOnly.
Display in Software Center, and only show notifications of computer restarts.
- HideAll.
Hide in Software Center and all notifications.

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
The acceptable values for this parameter are:

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
Indicates whether to enable write filters for embedded devices.
For a value of $True, the device commits changes during a maintenance window.
This action requires a restart.
For a value of $False, the device saves changes in an overlay and commits them later.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMSoftwareUpdateAutoDeploymentRule](./Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Enable-CMSoftwareUpdateAutoDeploymentRule](./Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Get-CMSoftwareUpdateAutoDeploymentRule](./Get-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](./Invoke-CMSoftwareUpdateAutoDeploymentRule.md)

[New-CMSoftwareUpdateAutoDeploymentRule](./New-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](./Remove-CMSoftwareUpdateAutoDeploymentRule.md)


