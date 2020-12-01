---
description: Create an application deployment.
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: New-CMApplicationDeployment
---

# New-CMApplicationDeployment

## SYNOPSIS

Create an application deployment.

## SYNTAX

### SearchByValueMandatory (Default)
```
New-CMApplicationDeployment [-AllowRepairApp <Boolean>] [-ApprovalRequired <Boolean>]
 [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>] [-DeployPurpose <DeployPurposeType>]
 [-DisableContentDependencyDetection] [-EnableMomAlert <Boolean>] [-EnableSoftDeadline <Boolean>]
 [-FailParameterValue <Int32>] [-GenerateScomAlertOnFailure <Boolean>] [-InputObject] <IResultObject>
 [-OverrideServiceWindow <Boolean>] [-PostponeDateTime <DateTime>] [-PreDeploy <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-ReplaceToastNotificationWithDialog <Boolean>] [-Simulation]
 [-SuccessParameterValue <Int32>] [-TimeBaseOn <TimeType>] [-UpdateSupersedence <Boolean>]
 [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMApplicationDeployment [-AllowRepairApp <Boolean>] [-ApprovalRequired <Boolean>]
 [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>] [-DeployPurpose <DeployPurposeType>]
 [-DisableContentDependencyDetection] [-EnableMomAlert <Boolean>] [-EnableSoftDeadline <Boolean>]
 [-FailParameterValue <Int32>] [-GenerateScomAlertOnFailure <Boolean>] [-Id] <Int32>
 [-OverrideServiceWindow <Boolean>] [-PostponeDateTime <DateTime>] [-PreDeploy <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-ReplaceToastNotificationWithDialog <Boolean>] [-Simulation]
 [-SuccessParameterValue <Int32>] [-TimeBaseOn <TimeType>] [-UpdateSupersedence <Boolean>]
 [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMApplicationDeployment [-AllowRepairApp <Boolean>] [-ApprovalRequired <Boolean>]
 [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>] [-DeployPurpose <DeployPurposeType>]
 [-DisableContentDependencyDetection] [-EnableMomAlert <Boolean>] [-EnableSoftDeadline <Boolean>]
 [-FailParameterValue <Int32>] [-GenerateScomAlertOnFailure <Boolean>] [-Name] <String>
 [-OverrideServiceWindow <Boolean>] [-PostponeDateTime <DateTime>] [-PreDeploy <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-ReplaceToastNotificationWithDialog <Boolean>] [-Simulation]
 [-SuccessParameterValue <Int32>] [-TimeBaseOn <TimeType>] [-UpdateSupersedence <Boolean>]
 [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMApplicationDeployment** cmdlet creates an application deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

{{ Add example description here }}

```powershell
{{ Add example code here }}
```

## PARAMETERS

### -AllowRepairApp

Applies to version 2002 and later. Use this parameter to configure the repair application option when creating a deployment for an application.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowUserRepairApplication

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Aliases: SupersedenceDeadlineDateTime

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

The site distributes content to the distribution point groups that are associated with this collection name.

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

### -ReplaceToastNotificationWithDialog

Specify whether to replace toast notifications with a more intrusive dialog window when a deployment requires a restart. It's an optional parameter and false by default.

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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
