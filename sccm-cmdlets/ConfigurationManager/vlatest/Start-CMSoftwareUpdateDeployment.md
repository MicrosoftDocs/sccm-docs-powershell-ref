---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: ABE2C372-76D4-46F7-B817-A963A5AA3145
---

# Start-CMSoftwareUpdateDeployment

## SYNOPSIS
Initiates a software update deployment in Configuration Manager.

## SYNTAX

### DeploySoftwareUpdateByValue (Default)
```
Start-CMSoftwareUpdateDeployment -InputObject <IResultObject> -CollectionName <String>
 [-DeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-EnforcementDeadlineDay <DateTime>] [-EnforcementDeadline <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>]
 [-DisableOperationsManagerAlert <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-ProtectedType <ProtectedType>] [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>] [-AcceptEula]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateByName
```
Start-CMSoftwareUpdateDeployment -SoftwareUpdateName <String> -CollectionName <String>
 [-DeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-EnforcementDeadlineDay <DateTime>] [-EnforcementDeadline <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>]
 [-DisableOperationsManagerAlert <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-ProtectedType <ProtectedType>] [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>] [-AcceptEula]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateById
```
Start-CMSoftwareUpdateDeployment -SoftwareUpdateId <String> -CollectionName <String> [-DeploymentName <String>]
 [-Description <String>] [-DeploymentType <DeploymentType>] [-SendWakeupPacket <Boolean>]
 [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>] [-DeploymentAvailableDay <DateTime>]
 [-DeploymentAvailableTime <DateTime>] [-EnforcementDeadlineDay <DateTime>] [-EnforcementDeadline <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>]
 [-DisableOperationsManagerAlert <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-ProtectedType <ProtectedType>] [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>] [-AcceptEula]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateGroupByName
```
Start-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName <String> -CollectionName <String>
 [-DeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-EnforcementDeadlineDay <DateTime>] [-EnforcementDeadline <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>]
 [-DisableOperationsManagerAlert <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-ProtectedType <ProtectedType>] [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>] [-AcceptEula]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateGroupById
```
Start-CMSoftwareUpdateDeployment -SoftwareUpdateGroupId <String> -CollectionName <String>
 [-DeploymentName <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-SendWakeupPacket <Boolean>] [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>]
 [-DeploymentAvailableDay <DateTime>] [-DeploymentAvailableTime <DateTime>]
 [-EnforcementDeadlineDay <DateTime>] [-EnforcementDeadline <DateTime>]
 [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>]
 [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>]
 [-DisableOperationsManagerAlert <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-ProtectedType <ProtectedType>] [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>] [-AcceptEula]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMSoftwareUpdateDeployment** cmdlet initiates a software update deployment.

## EXAMPLES

### Example 1: Start a required deployment by software update name
```
PS C:\>Start-CMSoftwareUpdateDeployment -SoftwareUpdateName "CT" -CollectionName "All Systems" -DeploymentName "Contoso-test" -Description "Contoso-test-deployment" -DeploymentType Required -SendWakeUpPacket $True -VerbosityLevel AllMessages -TimeBasedOn UTC -DeploymentAvailableDay 2012/10/24 -DeploymentAvailableTime 23:56 -DeploymentExpireDay 2013/10/21 -DeploymentExpireTime 11:20 -UserNotification HideAll -SoftwareInstallation $True -AllowRestart $True -RestartServer $True -RestartWorkstation $True -PersistOnWriteFilterDevice $False -GenerateSuccessAlert $True -PercentSuccess 90 -TimeValue 10 -TimeUnit Days -DisableOperationsManagerAlert $True -GenerateOperationsManagerAlert $True -ProtectedType RemoteDistributionPoint -UnprotectedType NoInstall -UseBranchCache $False -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True
```

This command starts a required software update deployment by using a software update name.

### Example 2: Start an available deployment by software update name
```
PS C:\>Start-CMSoftwareUpdateDeployment -SoftwareUpdateName "CT" -CollectionName "All Systems" -DeploymentName "Contoso-test2" -Description "Contoso-test2-deployment" -DeploymentType Available -VerbosityLevel AllMessages -TimeBasedOn UTC -DeploymentAvailableDay 2012/10/24 -DeploymentAvailableTime 23:56 -UserNotification DisplayAll -PersistOnWriteFilterDevice $False -DisableOperationsManagerAlert $True -GenerateOperationsManagerAlert $True -ProtectedType RemoteDistributionPoint -UnprotectedType NoInstall -UseBranchCache $False -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True
```

This command starts an available software update deployment by using a software update name.

### Example 3: Start a required deployment by software update group name
```
PS C:\>Start-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName "CTG" -CollectionName "All Systems" -DeploymentName "Contoso-test3" -Description "Contoso-test3-deployment" -DeploymentType Required -SendWakeUpPacket $True -VerbosityLevel AllMessages -TimeBasedOn UTC -DeploymentAvailableDay 2012/10/24 -DeploymentAvailableTime 23:56 -DeploymentExpireDay 2013/10/21 -DeploymentExpireTime 11:20 -UserNotification HideAll -SoftwareInstallation $True -AllowRestart $True -RestartServer $True -RestartWorkstation $True -PersistOnWriteFilterDevice $False -GenerateSuccessAlert $True -PercentSuccess 90 -TimeValue 10 -TimeUnit Days -DisableOperationsManagerAlert $True -GenerateOperationsManagerAlert $True -ProtectedType RemoteDistributionPoint -UnprotectedType NoInstall -UseBranchCache $False -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True
```

This command starts a software update deployment by using a collection name and an input object.

### Example 4: Start a deployment by software update group name
```
PS C:\>Start-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName "CTG" -CollectionName "All Systems" -DeploymentName "Contoso-test4" -Description "Contoso-test4-deployment" -DeploymentType Available -VerbosityLevel AllMessages -TimeBasedOn UTC -DeploymentAvailableDay 2012/10/24 -DeploymentAvailableTime 23:56 -UserNotification DisplayAll -PersistOnWriteFilterDevice $False -DisableOperationsManagerAlert $True -GenerateOperationsManagerAlert $True -ProtectedType RemoteDistributionPoint -UnprotectedType NoInstall -UseBranchCache $False -DownloadFromMicrosoftUpdate $True -AllowUseMeteredNetwork $True
```

This command starts a software update deployment by using a software update group name.

## PARAMETERS

### -AcceptEula


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

### -DeploymentAvailableDay


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

### -DownloadFromMicrosoftUpdate


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

### -GenerateOperationsManagerAlert


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

[Get-CMSoftwareUpdate](./Get-CMSoftwareUpdate.md)

[Get-CMSoftwareUpdateGroup](./Get-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdateDeployment](./Set-CMSoftwareUpdateDeployment.md)


