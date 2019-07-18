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
 

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1
```
PS XYZ:\>  
```

 

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
Aliases: UpdateGroupDeploymentName

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

### -UseMeteredNetwork
 

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

