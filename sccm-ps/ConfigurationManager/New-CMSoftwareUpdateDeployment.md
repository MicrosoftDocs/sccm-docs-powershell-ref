---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMSoftwareUpdateDeployment

## SYNOPSIS
Creates a software update deployment

## SYNTAX

### DeploySoftwareUpdateByValue (Default)
```
New-CMSoftwareUpdateDeployment -InputObject <IResultObject> [-DeploymentName <String>]
 [-SavedPackageId <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>] [-UserNotification <UserNotificationType>]
 [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>]
 [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-RequirePostRebootFullScan <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AcceptEula] [-DistributeContent]
 [-DistributeCollectionName <String>] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-Comment <String>] [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>]
 [-UseMeteredNetwork <Boolean>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateByName
```
New-CMSoftwareUpdateDeployment -SoftwareUpdateName <String> [-DeploymentName <String>]
 [-SavedPackageId <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>] [-UserNotification <UserNotificationType>]
 [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>]
 [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-RequirePostRebootFullScan <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AcceptEula] [-DistributeContent]
 [-DistributeCollectionName <String>] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-Comment <String>] [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>]
 [-UseMeteredNetwork <Boolean>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateById
```
New-CMSoftwareUpdateDeployment -SoftwareUpdateId <String> [-DeploymentName <String>] [-SavedPackageId <String>]
 [-Description <String>] [-DeploymentType <DeploymentType>] [-VerbosityLevel <VerbosityLevelType>]
 [-TimeBasedOn <TimeType>] [-UserNotification <UserNotificationType>] [-SoftwareInstallation <Boolean>]
 [-AllowRestart <Boolean>] [-RestartServer <Boolean>] [-RestartWorkstation <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>] [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>]
 [-DisableOperationsManagerAlert <Boolean>] [-GenerateOperationsManagerAlert <Boolean>]
 [-ProtectedType <ProtectedType>] [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>]
 [-RequirePostRebootFullScan <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AcceptEula]
 [-DistributeContent] [-DistributeCollectionName <String>] [-DistributionPointGroupName <String>]
 [-DistributionPointName <String>] [-Comment <String>] [-AvailableDateTime <DateTime>]
 [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeploySoftwareUpdateGroupByName
```
New-CMSoftwareUpdateDeployment -SoftwareUpdateGroupName <String> [-DeploymentName <String>]
 [-SavedPackageId <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>] [-UserNotification <UserNotificationType>]
 [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>]
 [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-RequirePostRebootFullScan <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AcceptEula] [-DistributeContent]
 [-DistributeCollectionName <String>] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-Comment <String>] [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>]
 [-UseMeteredNetwork <Boolean>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeploySoftwareUpdateGroupById
```
New-CMSoftwareUpdateDeployment -SoftwareUpdateGroupId <String> [-DeploymentName <String>]
 [-SavedPackageId <String>] [-Description <String>] [-DeploymentType <DeploymentType>]
 [-VerbosityLevel <VerbosityLevelType>] [-TimeBasedOn <TimeType>] [-UserNotification <UserNotificationType>]
 [-SoftwareInstallation <Boolean>] [-AllowRestart <Boolean>] [-RestartServer <Boolean>]
 [-RestartWorkstation <Boolean>] [-GenerateSuccessAlert <Boolean>] [-PercentSuccess <Int32>]
 [-TimeValue <Int32>] [-TimeUnit <TimeUnitType>] [-DisableOperationsManagerAlert <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-ProtectedType <ProtectedType>]
 [-UnprotectedType <UnprotectedType>] [-UseBranchCache <Boolean>] [-RequirePostRebootFullScan <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-AcceptEula] [-DistributeContent]
 [-DistributeCollectionName <String>] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-Comment <String>] [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>]
 [-UseMeteredNetwork <Boolean>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AcceptEula
{{Fill AcceptEula Description}}

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
{{Fill AllowRestart Description}}

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
{{Fill AvailableDateTime Description}}

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
{{Fill Collection Description}}

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
{{Fill CollectionId Description}}

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
{{Fill CollectionName Description}}

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
{{Fill Comment Description}}

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
{{Fill DeadlineDateTime Description}}

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
{{Fill DeploymentName Description}}

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
{{Fill DeploymentType Description}}

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
{{Fill Description Description}}

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
{{Fill DisableOperationsManagerAlert Description}}

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

### -DistributeCollectionName
{{Fill DistributeCollectionName Description}}

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
{{Fill DistributeContent Description}}

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
{{Fill DistributionPointGroupName Description}}

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
{{Fill DistributionPointName Description}}

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
{{Fill DownloadFromMicrosoftUpdate Description}}

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
{{Fill GenerateOperationsManagerAlert Description}}

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
{{Fill GenerateSuccessAlert Description}}

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
{{Fill InputObject Description}}

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
{{Fill PercentSuccess Description}}

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
{{Fill PersistOnWriteFilterDevice Description}}

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
{{Fill ProtectedType Description}}

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
{{Fill RequirePostRebootFullScan Description}}

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
{{Fill RestartServer Description}}

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
{{Fill RestartWorkstation Description}}

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
{{Fill SavedPackageId Description}}

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
{{Fill SendWakeupPacket Description}}

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
{{Fill SoftwareInstallation Description}}

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
{{Fill SoftwareUpdateGroupId Description}}

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
{{Fill SoftwareUpdateGroupName Description}}

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
{{Fill SoftwareUpdateId Description}}

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
{{Fill SoftwareUpdateName Description}}

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
{{Fill TimeBasedOn Description}}

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
{{Fill TimeUnit Description}}

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
{{Fill TimeValue Description}}

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
{{Fill UnprotectedType Description}}

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
{{Fill UseBranchCache Description}}

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
{{Fill UseMeteredNetwork Description}}

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
{{Fill UserNotification Description}}

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
{{Fill VerbosityLevel Description}}

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

