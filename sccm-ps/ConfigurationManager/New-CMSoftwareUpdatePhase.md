---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMSoftwareUpdatePhase

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByCollection
```
New-CMSoftwareUpdatePhase [-UserNotificationOption <UserNotificationType>] [-SoftwareInstallation <Boolean>]
 [-AllowSystemRestart <Boolean>] [-WriteFilterCommit <Boolean>] [-PhaseDescription <String>]
 [-EnableWakeOnLan <Boolean>] [-StateMessageVerbosity <VerbosityLevelType>]
 [-ServerRestartSuppression <Boolean>] [-WorkstationRestartSuppression <Boolean>]
 [-RequirePostRebootFullScan <Boolean>] [-EnableAlert <Boolean>] [-AlertThresholdPercentage <Int32>]
 [-AlertDelta <Int32>] [-AlertUnit <TimeUnitType>] [-DisableSCOMAlert <Boolean>]
 [-GenerateSCOMAlertOnFailure <Boolean>] [-UseNeighborDP <Boolean>] [-UseSiteDefaultDP <Boolean>]
 [-AllowWUMUFallback <Boolean>] [-AllowMeteredConnection <Boolean>] -PhaseName <String>
 [-Collection] <IResultObject> [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>]
 [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>] [-ThrottlingDays <Int32>]
 [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByCollectionId
```
New-CMSoftwareUpdatePhase [-UserNotificationOption <UserNotificationType>] [-SoftwareInstallation <Boolean>]
 [-AllowSystemRestart <Boolean>] [-WriteFilterCommit <Boolean>] [-PhaseDescription <String>]
 [-EnableWakeOnLan <Boolean>] [-StateMessageVerbosity <VerbosityLevelType>]
 [-ServerRestartSuppression <Boolean>] [-WorkstationRestartSuppression <Boolean>]
 [-RequirePostRebootFullScan <Boolean>] [-EnableAlert <Boolean>] [-AlertThresholdPercentage <Int32>]
 [-AlertDelta <Int32>] [-AlertUnit <TimeUnitType>] [-DisableSCOMAlert <Boolean>]
 [-GenerateSCOMAlertOnFailure <Boolean>] [-UseNeighborDP <Boolean>] [-UseSiteDefaultDP <Boolean>]
 [-AllowWUMUFallback <Boolean>] [-AllowMeteredConnection <Boolean>] -PhaseName <String>
 [-CollectionId] <String> [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>]
 [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>] [-ThrottlingDays <Int32>]
 [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByCollectionName
```
New-CMSoftwareUpdatePhase [-UserNotificationOption <UserNotificationType>] [-SoftwareInstallation <Boolean>]
 [-AllowSystemRestart <Boolean>] [-WriteFilterCommit <Boolean>] [-PhaseDescription <String>]
 [-EnableWakeOnLan <Boolean>] [-StateMessageVerbosity <VerbosityLevelType>]
 [-ServerRestartSuppression <Boolean>] [-WorkstationRestartSuppression <Boolean>]
 [-RequirePostRebootFullScan <Boolean>] [-EnableAlert <Boolean>] [-AlertThresholdPercentage <Int32>]
 [-AlertDelta <Int32>] [-AlertUnit <TimeUnitType>] [-DisableSCOMAlert <Boolean>]
 [-GenerateSCOMAlertOnFailure <Boolean>] [-UseNeighborDP <Boolean>] [-UseSiteDefaultDP <Boolean>]
 [-AllowWUMUFallback <Boolean>] [-AllowMeteredConnection <Boolean>] -PhaseName <String>
 [-CollectionName] <String> [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>]
 [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>] [-ThrottlingDays <Int32>]
 [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AlertDelta
{{ Fill AlertDelta Description }}

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

### -AlertThresholdPercentage
{{ Fill AlertThresholdPercentage Description }}

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

### -AlertUnit
{{ Fill AlertUnit Description }}

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

### -AllowMeteredConnection
{{ Fill AllowMeteredConnection Description }}

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

### -AllowSystemRestart
{{ Fill AllowSystemRestart Description }}

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

### -AllowWUMUFallback
{{ Fill AllowWUMUFallback Description }}

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

### -BeginCondition
{{ Fill BeginCondition Description }}

```yaml
Type: BeginConditionType
Parameter Sets: (All)
Aliases:
Accepted values: AfterPeriod, Manually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection
{{ Fill Collection Description }}

```yaml
Type: IResultObject
Parameter Sets: SearchByCollection
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
{{ Fill CollectionId Description }}

```yaml
Type: String
Parameter Sets: SearchByCollectionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
{{ Fill CollectionName Description }}

```yaml
Type: String
Parameter Sets: SearchByCollectionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CriteriaOption
{{ Fill CriteriaOption Description }}

```yaml
Type: CriteriaType
Parameter Sets: (All)
Aliases:
Accepted values: Compliance, Number

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CriteriaValue
{{ Fill CriteriaValue Description }}

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

### -DaysAfterPreviousPhaseSuccess
{{ Fill DaysAfterPreviousPhaseSuccess Description }}

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

### -DeadlineUnit
{{ Fill DeadlineUnit Description }}

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

### -DeadlineValue
{{ Fill DeadlineValue Description }}

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

### -DisableSCOMAlert
{{ Fill DisableSCOMAlert Description }}

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
{{ Fill DisableWildcardHandling Description }}

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

### -EnableAlert
{{ Fill EnableAlert Description }}

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

### -EnableWakeOnLan
{{ Fill EnableWakeOnLan Description }}

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
{{ Fill ForceWildcardHandling Description }}

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

### -GenerateSCOMAlertOnFailure
{{ Fill GenerateSCOMAlertOnFailure Description }}

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

### -InstallationChoice
{{ Fill InstallationChoice Description }}

```yaml
Type: InstallationChoiceType
Parameter Sets: (All)
Aliases:
Accepted values: AsSoonAsPossible, AfterPeriod

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PhaseDescription
{{ Fill PhaseDescription Description }}

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

### -PhaseName
{{ Fill PhaseName Description }}

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

### -RequirePostRebootFullScan
{{ Fill RequirePostRebootFullScan Description }}

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

### -ServerRestartSuppression
{{ Fill ServerRestartSuppression Description }}

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
{{ Fill SoftwareInstallation Description }}

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

### -StateMessageVerbosity
{{ Fill StateMessageVerbosity Description }}

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

### -ThrottlingDays
{{ Fill ThrottlingDays Description }}

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

### -UseNeighborDP
{{ Fill UseNeighborDP Description }}

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

### -UserNotificationOption
{{ Fill UserNotificationOption Description }}

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

### -UseSiteDefaultDP
{{ Fill UseSiteDefaultDP Description }}

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

### -WorkstationRestartSuppression
{{ Fill WorkstationRestartSuppression Description }}

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

### -WriteFilterCommit
{{ Fill WriteFilterCommit Description }}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManager.PhasedDeploymentModel.Phase

## NOTES

## RELATED LINKS
