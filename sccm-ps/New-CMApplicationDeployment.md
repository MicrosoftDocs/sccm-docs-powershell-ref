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
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -ApprovalRequired
{{Fill ApprovalRequired Description}}

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

### -DeployAction
{{Fill DeployAction Description}}

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
{{Fill DeployPurpose Description}}

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
{{Fill DisableContentDependencyDetection Description}}

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

### -EnableMomAlert
{{Fill EnableMomAlert Description}}

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
{{Fill EnableSoftDeadline Description}}

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
{{Fill FailParameterValue Description}}

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
{{Fill GenerateScomAlertOnFailure Description}}

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
{{Fill Id Description}}

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
{{Fill InputObject Description}}

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
{{Fill Name Description}}

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
{{Fill OverrideServiceWindow Description}}

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

### -PostponeDateTime
{{Fill PostponeDateTime Description}}

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
{{Fill PreDeploy Description}}

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
{{Fill RebootOutsideServiceWindow Description}}

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

### -Simulation
{{Fill Simulation Description}}

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
{{Fill SuccessParameterValue Description}}

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
{{Fill TimeBaseOn Description}}

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
{{Fill UpdateSupersedence Description}}

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

