---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMApplicationDeployment

## SYNOPSIS
Creates an application deployment

## SYNTAX

### SearchByValueMandatory (Default)
```
New-CMApplicationDeployment [-InputObject] <IResultObject> [-ApprovalRequired <Boolean>]
 [-DeployAction <DeployActionType>] [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>]
 [-FailParameterValue <Int32>] [-OverrideServiceWindow <Boolean>] [-PostponeDateTime <DateTime>]
 [-PreDeploy <Boolean>] [-GenerateScomAlertOnFailure <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-SuccessParameterValue <Int32>] [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>]
 [-DisableContentDependencyDetection] [-UpdateSupersedence <Boolean>] [-Simulation]
 [-EnableSoftDeadline <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMApplicationDeployment [-Name] <String> [-ApprovalRequired <Boolean>] [-DeployAction <DeployActionType>]
 [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>] [-FailParameterValue <Int32>]
 [-OverrideServiceWindow <Boolean>] [-PostponeDateTime <DateTime>] [-PreDeploy <Boolean>]
 [-GenerateScomAlertOnFailure <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-SuccessParameterValue <Int32>] [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>]
 [-DisableContentDependencyDetection] [-UpdateSupersedence <Boolean>] [-Simulation]
 [-EnableSoftDeadline <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMApplicationDeployment [-Id] <Int32> [-ApprovalRequired <Boolean>] [-DeployAction <DeployActionType>]
 [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>] [-FailParameterValue <Int32>]
 [-OverrideServiceWindow <Boolean>] [-PostponeDateTime <DateTime>] [-PreDeploy <Boolean>]
 [-GenerateScomAlertOnFailure <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-SuccessParameterValue <Int32>] [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>]
 [-DisableContentDependencyDetection] [-UpdateSupersedence <Boolean>] [-Simulation]
 [-EnableSoftDeadline <Boolean>] [-DistributeContent] [-DistributeCollectionName <String>]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-Comment <String>]
 [-AvailableDateTime <DateTime>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
```

 

## PARAMETERS

### -ApprovalRequired
 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AppRequiresApproval

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

### -DeployAction
 

```yaml
Type: DeployActionType
Parameter Sets: (All)
Aliases: 
Accepted values: Install, Uninstall

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

### -DisableContentDependencyDetection
 

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableDetectAssociatedContentDependencies

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

### -EnableMomAlert
 

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

### -EnableSoftDeadline
 

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

### -FailParameterValue
 

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

### -GenerateScomAlertOnFailure
 

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RaiseMomAlertsOnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
 

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID, ApplicationId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
 

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Application

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
 

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName, ApplicationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideServiceWindow
 

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

### -PostponeDateTime
 

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

### -PreDeploy
 

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

### -RebootOutsideServiceWindow
 

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

### -Simulation
 

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

### -SuccessParameterValue
 

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

### -TimeBaseOn
 

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

### -UpdateSupersedence
 

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

