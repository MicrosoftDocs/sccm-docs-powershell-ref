---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
online version:
schema: 2.0.0
---

# New-CMTaskSequencePhase

## SYNOPSIS

Use this cmdlet to create a deployment phase for a task sequence.

## SYNTAX

### SearchByCollection
```
New-CMTaskSequencePhase [-AllowFallback <Boolean>] [-AllowRemoteDP <Boolean>] [-AllowSystemRestart <Boolean>]
 [-BeginCondition <BeginConditionType>] [-Collection] <IResultObject> [-Comments <String>]
 [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>] [-DeploymentOption <DeploymentOptionType>]
 [-InstallationChoice <InstallationChoiceType>] -PhaseName <String> [-PreDownload <Boolean>]
 [-SoftwareInstallation <Boolean>] [-ThrottlingDays <Int32>] [-UserNotification <UserNotificationType>]
 [-WriteFilterCommit <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByCollectionId
```
New-CMTaskSequencePhase [-AllowFallback <Boolean>] [-AllowRemoteDP <Boolean>] [-AllowSystemRestart <Boolean>]
 [-BeginCondition <BeginConditionType>] [-CollectionId] <String> [-Comments <String>]
 [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>] [-DeploymentOption <DeploymentOptionType>]
 [-InstallationChoice <InstallationChoiceType>] -PhaseName <String> [-PreDownload <Boolean>]
 [-SoftwareInstallation <Boolean>] [-ThrottlingDays <Int32>] [-UserNotification <UserNotificationType>]
 [-WriteFilterCommit <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByCollectionName
```
New-CMTaskSequencePhase [-AllowFallback <Boolean>] [-AllowRemoteDP <Boolean>] [-AllowSystemRestart <Boolean>]
 [-BeginCondition <BeginConditionType>] [-CollectionName] <String> [-Comments <String>]
 [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>] [-DeploymentOption <DeploymentOptionType>]
 [-InstallationChoice <InstallationChoiceType>] -PhaseName <String> [-PreDownload <Boolean>]
 [-SoftwareInstallation <Boolean>] [-ThrottlingDays <Int32>] [-UserNotification <UserNotificationType>]
 [-WriteFilterCommit <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to create a deployment phase for a task sequence.

## EXAMPLES

### Example 1: Create a task sequence phase

This example creates a task sequence phase named **MyTSPhase** for the collection named **MyCollection**.

```powershell
New-CMTaskSequencePhase -CollectionName "MyCollection" -PhaseName "MyTSPhase" -UserNotification DisplayAll -AllowRemoteDP $true
```

## PARAMETERS

### -AllowFallback

This parameter is the same as the following setting on the **Distribution Points** page of the **Add Phase Wizard** in the console: **Allow clients to use distribution points from the default site boundary group**.

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

### -AllowRemoteDP

This parameter is the same as the following setting on the **Distribution Points** page of the **Add Phase Wizard** in the console: **When no local distribution point is available, use a remote distribution point**.

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

This parameter is the same as the following setting on the **User Experience** page of the **Add Phase Wizard** in the console: **System restart (if required to complete installation)**. This setting applies when the installation deadline is reached, to allow this activity to be performed outside the maintenance window.

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

Specify an option for beginning this phase of deployment after success of the previous phase:

- `AfterPeriod`: This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Automatically begin this phase after a deferral period (in days)**. If you specify this value, use **DaysAfterPreviousPhaseSuccess** to configure the period of time.

- `Manually`: This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Manually begin this phase of deployment**.

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

Specify an object for the target collection

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

Specify the target collection by ID.

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

Specify the target collection by name.

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

### -Comments

Specify optional comments for this phase. The maximum length is 512 characters.

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

### -CriteriaOption

Specify an option to choose the criteria for success of the previous phase:

- `Compliance`: This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Deployment success percentage**. Specify the percentage value with the **CriteriaValue** parameter.

- `Number`: This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Number of devices successfully deployed**. Specify the number of devices with the **CriteriaValue** parameter.

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

This integer value depends upon the value that you specify for **CriteriaOption**:

- `Compliance`: Specify the percentage

- `Number`: Specify the number of devices

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

Specify an integer value for the number of days after success of the previous phase to begin this phase. This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Automatically begin this phase after a deferral period (in days)**.

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

Specify the type of deadline period. Use this parameter with **DeadlineValue**.

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

This parameter is only used if you specify `AfterPeriod` with the **InstallationChoice** parameter.

Specify an integer value for the period of time for the deadline. Use the **DeadlineUnit** parameter to specify the type of period: `Hours`, `Days`, `Weeks`, `Months`. This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Installation is required after this period of time**.

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

### -DeploymentOption

This parameter is the same as the following setting on the **Distribution Points** page of the **Add Phase Wizard** in the console: **Select the deployment option to use when a client uses a distribution point from a neighbor boundary group or the default site boundary group**. It accepts the following values:

- `DownloadContentLocallyWhenNeededByRunningTaskSequence`: Download content locally when needed by the running task sequence
- `DownloadAllContentLocallyBeforeStartingTaskSequence`: Download all content locally before starting task sequence

```yaml
Type: DeploymentOptionType
Parameter Sets: (All)
Aliases:
Accepted values: DownloadContentLocallyWhenNeededByRunningTaskSequence, DownloadAllContentLocallyBeforeStartingTaskSequence

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

### -InstallationChoice

Specify an option for the behavior relative to when the software is made available:

- `AsSoonAsPossible`: This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Installation is required as soon as possible**.

- `AfterPeriod`: This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Installation is required after this period of time**. If you specify this value, use **DeadlineUnit** and **DeadlineValue** to configure the period of time.

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

### -PhaseName

Specify a name for the phase.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreDownload

This parameter is the same as the following setting on the **General** page of the **Add Phase Wizard** in the console: **Pre-download content for this task sequence**.

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

This parameter is the same as the following setting on the **User Experience** page of the **Add Phase Wizard** in the console: **Software Installation**. This setting applies when the installation deadline is reached, to allow this activity to be performed outside the maintenance window.

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

### -ThrottlingDays

Specify an integer value for the number of days to gradually make this software available. This parameter is the same as the following setting on the **Phase Settings** page of the **Add Phase Wizard** in the console: **Gradually make this software available over this period of time (in days)**.

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

### -UserNotification

This parameter is the same as the following setting on the **User Experience** page of the **Add Phase Wizard** in the console: **Specify user experience setting for this deployment** with the following values:

- `DisplayAll`: Display in Software Center and show all notifications
- `HideAll`: Hide in Software Center and all notifications

```yaml
Type: UserNotificationType
Parameter Sets: (All)
Aliases:
Accepted values: DisplayAll, HideAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WriteFilterCommit

This parameter is the same as the following setting on the **User Experience** page of the **Add Phase Wizard** in the console: **Commit changes at deadline or during a maintenance window (requires restart)**. This setting applies to write filter handling for Windows Embedded devices.

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

### None

## OUTPUTS

### Microsoft.ConfigurationManager.PhasedDeploymentModel.Phase

## NOTES

## RELATED LINKS
