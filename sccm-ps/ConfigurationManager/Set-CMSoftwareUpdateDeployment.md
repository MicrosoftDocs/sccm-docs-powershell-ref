---
external help file: AdminUI.PS.Deployments.dll-Help.xml
ms.assetid: B274271A-FA5D-4272-A981-049DE05A419C
online version: https://go.microsoft.com/fwlink/?linkid=834074
schema: 2.0.0
---

# Set-CMSoftwareUpdateDeployment

## SYNOPSIS
Modifies a software update deployment in Configuration Manager.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMSoftwareUpdateDeployment -InputObject <IResultObject> [-DeploymentName <String>]
 [-NewDeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-AvailableDateTime <DateTime>] [-AlertDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-Enable <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-PassThru]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdateDeploymentByNameMandatory
```
Set-CMSoftwareUpdateDeployment -SoftwareUpdateName <String> [-DeploymentName <String>]
 [-NewDeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-AvailableDateTime <DateTime>] [-AlertDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-Enable <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-PassThru]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdateDeploymentByIdMandatory
```
Set-CMSoftwareUpdateDeployment -SoftwareUpdateId <String> [-DeploymentName <String>]
 [-NewDeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-AvailableDateTime <DateTime>] [-AlertDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-Enable <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-PassThru]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdateGroupDeploymentByNameMandatory
```
Set-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName <String> [-DeploymentName <String>]
 [-NewDeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-AvailableDateTime <DateTime>] [-AlertDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-Enable <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-PassThru]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdateGroupDeploymentByIdMandatory
```
Set-CMSoftwareUpdateDeployment -SoftwareUpdateGroupId <String> [-DeploymentName <String>]
 [-NewDeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-AvailableDateTime <DateTime>] [-AlertDateTime <DateTime>] [-DeploymentExpireDateTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>]
 [-AllowUseMeteredNetwork <Boolean>] [-Enable <Boolean>] [-RequirePostRebootFullScan <Boolean>] [-PassThru]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdateDeployment** cmdlet modifies a deployment of software updates in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Set a deployment with expiration time
```
PS C:\> Set-CMSoftwareUpdateDeployment -SoftwareUpdateName "CT" -DeploymentName "Contoso-test1" -NewDeploymentName "Contoso-test5" -Description "Contoso-test5-deployment" -CollectionName "All Mobile Devices" -SendWakeUpPacket $False -VerbosityLevel OnlySuccessAndErrorMessages -TimeBasedOn LocalTime -DeploymentAvailableDay 2013/11/24 -DeploymentAvailableTime 13:26 -DeploymentExpireDay 2014/7/22 -DeploymentExpireTime 4:30 -UserNotification DisplayAll -SoftwareInstallation $False -AllowRestart $False -RestartServer $False -RestartWorkstation $False -PersistOnWriteFilterDevice $True -GenerateSuccessAlert $False -PercentSuccess 99  -DisableOperationsManagerAlert $False -GenerateOperationsManagerAlert $False -ProtectedType NoInstall -UnprotectedType UnprotectedDistributionPoint -UseBranchCache $True -DownloadFromMicrosoftUpdate $False -AllowUseMeteredNetwork $False
```

This command sets a software update deployment by using a software update name and expiration time.

### Example 2: Start a deployment without expiration time
```
PS C:\> Set-CMSoftwareUpdateDeployment -SoftwareUpdateName "CT" -DeploymentName "Contoso-test2" -NewDeploymentName "Contoso-test6" -Description "Contoso-test6-deployment" -CollectionName "All Mobile Devices" -VerbosityLevel OnlyErrorMessages -TimeBasedOn LocalTime -DeploymentAvailableDay 2013/12/24 -DeploymentAvailableTime 3:56 -UserNotification DisplaySoftwareCenterOnly -PersistOnWriteFilterDevice $True -DisableOperationsManagerAlert $False -GenerateOperationsManagerAlert $False -ProtectedType NoInstall -UnprotectedType UnprotectedDistributionPoint -UseBranchCache $True -DownloadFromMicrosoftUpdate $False -AllowUseMeteredNetwork $False
```

This command sets a software update deployment by using a software update name but no specified expiration time.

### Example 3: Start a deployment by software update group name and expiration time
```
PS C:\> Set-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName "CTG" -DeploymentName "Contoso-test3" -NewDeploymentName "Contoso-test7" -Description "Contoso-test7-deployment" -CollectionName "All Mobile Devices" -SendWakeUpPacket $False -VerbosityLevel OnlySuccessAndErrorMessages -TimeBasedOn LocalTime -DeploymentAvailableDay 2013/11/24 -DeploymentAvailableTime 13:26 -DeploymentExpireDay 2014/7/22 -DeploymentExpireTime 4:30 -UserNotification DisplayAll -SoftwareInstallation $False -AllowRestart $False -RestartServer $False -RestartWorkstation $False -PersistOnWriteFilterDevice $True -GenerateSuccessAlert $False -PercentSuccess 99  -DisableOperationsManagerAlert $False -GenerateOperationsManagerAlert $False -ProtectedType NoInstall -UnprotectedType UnprotectedDistributionPoint -UseBranchCache $True -DownloadFromMicrosoftUpdate $False -AllowUseMeteredNetwork $False
```

This command sets a software update deployment by using a software update group name and an expiration time.

### Example 4: Start a deployment by software update group name
```
PS C:\> Set-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName "CTG" -DeploymentName "Contoso-test4" -NewDeploymentName "Contoso-test8" -Description "Contoso-test8-deployment" -CollectionName "All Mobile Devices" -VerbosityLevel OnlyErrorMessages -TimeBasedOn LocalTime -DeploymentAvailableDay 2013/12/24 -DeploymentAvailableTime 3:56 -UserNotification DisplaySoftwareCenterOnly -PersistOnWriteFilterDevice $True -DisableOperationsManagerAlert $False -GenerateOperationsManagerAlert $False -ProtectedType NoInstall -UnprotectedType UnprotectedDistributionPoint -UseBranchCache $True -DownloadFromMicrosoftUpdate $False -AllowUseMeteredNetwork $False
```

This command starts a software update deployment by using a software update group name but no specified expiration time.

## PARAMETERS

### -AlertDateTime
 

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
Specifies a name of a collection in Configuration Manager.
A collection is a group of client computers.

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

### -DeploymentExpireDateTime
 

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
Indicates whether the cmdlet enables software updates in Configuration Manager.

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
Parameter Sets: SetByValueMandatory
Aliases: SoftwareUpdate, DeploymentSummary, SoftwareUpdateGroup, Assignment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NewDeploymentName
Specifies a name for a new deployment in Configuration Manager.

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
Specifies a percentage of the update.

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

### -RequirePostRebootFullScan
 

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
Specifies a verbosity level type, such as error messages.
The acceptable values for this parameter are:

- AllMessages
- OnlyErrorMessages
- OnlySuccessandErrorMessages

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

[Start-CMSoftwareUpdateDeployment](Start-CMSoftwareUpdateDeployment.md)
