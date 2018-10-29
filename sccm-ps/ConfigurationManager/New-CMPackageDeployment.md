---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMPackageDeployment

## SYNOPSIS
Creates a package deployment

## SYNTAX

### DeployStandardProgramByPackageValue (Default)
```
New-CMPackageDeployment [-StandardProgram] [-Package] <IResultObject> -ProgramName <String>
 [-DeployPurpose <DeployPurposeType>] [-SendWakeupPacket <Boolean>] [-UseUtcForAvailableSchedule <Boolean>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-FastNetworkOption <FastNetworkOptionType>] [-SlowNetworkOption <SlowNetworkOptionType>]
 [-AllowSharedContent <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageName
```
New-CMPackageDeployment [-DeviceProgram] -PackageName <String> -ProgramName <String>
 [-DeployPurpose <DeployPurposeType>] [-UseUtc <Boolean>] [-RecurValue <Int32>] [-RecurUnit <RecurUnitType>]
 [-Rerun <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageId
```
New-CMPackageDeployment [-DeviceProgram] -PackageId <String> -ProgramName <String>
 [-DeployPurpose <DeployPurposeType>] [-UseUtc <Boolean>] [-RecurValue <Int32>] [-RecurUnit <RecurUnitType>]
 [-Rerun <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageValue
```
New-CMPackageDeployment [-DeviceProgram] [-Package] <IResultObject> -ProgramName <String>
 [-DeployPurpose <DeployPurposeType>] [-UseUtc <Boolean>] [-RecurValue <Int32>] [-RecurUnit <RecurUnitType>]
 [-Rerun <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByProgramValue
```
New-CMPackageDeployment [-DeviceProgram] [-Program] <IResultObject> [-DeployPurpose <DeployPurposeType>]
 [-SendWakeupPacket <Boolean>] [-UseUtc <Boolean>] [-RecurValue <Int32>] [-RecurUnit <RecurUnitType>]
 [-Rerun <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployStandardProgramByPackageName
```
New-CMPackageDeployment [-StandardProgram] -PackageName <String> -ProgramName <String>
 [-DeployPurpose <DeployPurposeType>] [-SendWakeupPacket <Boolean>] [-UseUtcForAvailableSchedule <Boolean>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-FastNetworkOption <FastNetworkOptionType>] [-SlowNetworkOption <SlowNetworkOptionType>]
 [-AllowSharedContent <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployStandardProgramByPackageId
```
New-CMPackageDeployment [-StandardProgram] -PackageId <String> -ProgramName <String>
 [-DeployPurpose <DeployPurposeType>] [-SendWakeupPacket <Boolean>] [-UseUtcForAvailableSchedule <Boolean>]
 [-UseUtcForExpireSchedule <Boolean>] [-ScheduleEvent <ScheduleEventType>] [-Schedule <IResultObject[]>]
 [-RerunBehavior <RerunBehaviorType>] [-RunFromSoftwareCenter <Boolean>] [-SoftwareInstallation <Boolean>]
 [-SystemRestart <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-FastNetworkOption <FastNetworkOptionType>] [-SlowNetworkOption <SlowNetworkOptionType>]
 [-AllowSharedContent <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployStandardProgramByProgramValue
```
New-CMPackageDeployment [-StandardProgram] [-Program] <IResultObject> [-DeployPurpose <DeployPurposeType>]
 [-SendWakeupPacket <Boolean>] [-UseUtcForAvailableSchedule <Boolean>] [-UseUtcForExpireSchedule <Boolean>]
 [-ScheduleEvent <ScheduleEventType>] [-Schedule <IResultObject[]>] [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-SoftwareInstallation <Boolean>] [-SystemRestart <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-FastNetworkOption <FastNetworkOptionType>]
 [-SlowNetworkOption <SlowNetworkOptionType>] [-AllowSharedContent <Boolean>] [-DistributeContent]
 [-DistributeCollectionName <String>] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-Comment <String>] [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>]
 [-UseMeteredNetwork <Boolean>] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
```

 

## PARAMETERS

### -AllowSharedContent
 

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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

### -DeployPurpose
 

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

### -DeviceProgram
 

```yaml
Type: SwitchParameter
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 

Required: True
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

### -FastNetworkOption
 

```yaml
Type: FastNetworkOptionType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 
Accepted values: RunProgramFromDistributionPoint, DownloadContentFromDistributionPointAndRunLocally

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

### -Package
 

```yaml
Type: IResultObject
Parameter Sets: DeployStandardProgramByPackageValue, DeployDeviceProgramByPackageValue
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PackageId
 

```yaml
Type: String
Parameter Sets: DeployDeviceProgramByPackageId, DeployStandardProgramByPackageId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName
 

```yaml
Type: String
Parameter Sets: DeployDeviceProgramByPackageName, DeployStandardProgramByPackageName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistOnWriteFilterDevice
 

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Program
 

```yaml
Type: IResultObject
Parameter Sets: DeployDeviceProgramByProgramValue, DeployStandardProgramByProgramValue
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProgramName
 

```yaml
Type: String
Parameter Sets: DeployStandardProgramByPackageValue, DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId
Aliases: StandardProgramName, DeviceProgramName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurUnit
 

```yaml
Type: RecurUnitType
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 
Accepted values: Minutes, Hours, Days

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurValue
 

```yaml
Type: Int32
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rerun
 

```yaml
Type: Boolean
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RerunBehavior
 

```yaml
Type: RerunBehaviorType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 
Accepted values: NeverRerunDeployedProgram, AlwaysRerunProgram, RerunIfFailedPreviousAttempt, RerunIfSucceededOnPreviousAttempt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunFromSoftwareCenter
 

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: AllowUsersRunIndependently

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
 

```yaml
Type: IResultObject[]
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScheduleEvent
 

```yaml
Type: ScheduleEventType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 
Accepted values: AsSoonAsPossible, LogOn, LogOff

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendWakeupPacket
 

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployDeviceProgramByProgramValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SlowNetworkOption
 

```yaml
Type: SlowNetworkOptionType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 
Accepted values: DoNotRunProgram, DownloadContentFromDistributionPointAndLocally, RunProgramFromDistributionPoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInstallation
 

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardProgram
 

```yaml
Type: SwitchParameter
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemRestart
 

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
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

### -UseUtc
 

```yaml
Type: Boolean
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtcForAvailableSchedule
 

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtcForExpireSchedule
 

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: 

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

