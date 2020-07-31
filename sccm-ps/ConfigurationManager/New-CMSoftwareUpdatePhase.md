---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMSoftwareUpdatePhase

## SYNOPSIS

Use this cmdlet to create a deployment phase for software update.

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

Starting in version 2002, use this cmdlet to create a deployment phase for software update.

## EXAMPLES

### Example 1: Create a software update phase

This example creates a software update phase named **MySUPhase** for the collection named **MyCollection** that will only display in Software Center.

```powershell
New-CMSoftwareUpdatePhase `
 -CollectionName "MyCollection" `
 -PhaseName "MySUPhase" `
 -UserNotificationOption DisplaySoftwareCenterOnly
```

## PARAMETERS

### -AlertDelta

This parameter is the same as the following setting on the **Alerts** page of the **Add Phase Wizard** in the console: **Offset from the deadline time**. Specify an integer value for the offset, and then specify the period type with the **AlertUnit** parameter.

To set this value, you have to use the **EnableAlert** parameter.

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

This parameter is the same as the following setting on the **Alerts** page of the **Add Phase Wizard** in the console: **Client compliance is below the following (percent)**. Specify an integer value for the percentage. To set this value, you have to use the **EnableAlert** parameter.

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

Specify the type of period. Use this parameter with **AlertDelta**.

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

This parameter is the same as the following setting on the **Download Settings** page of the **Add Phase Wizard** in the console: **Allow clients on a metered internet connection to download content after the installation deadline, which might incur additional costs**.

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

### -AllowWUMUFallback

This parameter is the same as the following setting on the **Download Settings** page of the **Add Phase Wizard** in the console: **If software updates are not available on distribution point in current, neighbor or site boundary groups, download content from Microsoft Updates**.

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

Specify an object for the target collection.

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

### -DisableSCOMAlert

This parameter is the same as the following setting on the **Alerts** page of the **Add Phase Wizard** in the console: **Disable Operations Manager alerts while software updates run**.

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

### -EnableAlert

This parameter is the same as the following setting on the **Alerts** page of the **Add Phase Wizard** in the console: **Generate an alert when the following conditions are met**. When you set this parameter to `$true`, also set the following parameters:

- AlertThresholdPercentage
- AlertDelta

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

This parameter is the same as the following setting on the **Deployment Settings** page of the **Add Phase Wizard** in the console: **Use Wake-on-LAN to wake up clients for required deployments**.

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

### -GenerateSCOMAlertOnFailure

This parameter is the same as the following setting on the **Alerts** page of the **Add Phase Wizard** in the console: **Generate Operations Manager alert when a software update installation fails**.

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

### -PhaseDescription

Specify a description for the phase.

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

Specify a name for the description.

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

This parameter is the same as the following setting on the **User Experience** page of the **Add Phase Wizard** in the console: **If any update in this deployment requires a system restart, run updates deployment evaluation cycle after restart**.

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

This parameter is the same as the following setting on the **User Experience** page of the **Add Phase Wizard** in the console. Suppress the system restart on the following devices: **Servers**.

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

### -StateMessageVerbosity

This parameter is the same as the following setting on the **Deployment Settings** page of the **Add Phase Wizard** in the console: **State message detail level** with the following values:

- `AllMessages`: All messages
- `OnlySuccessAndErrorMessages`: Only success and error messages
- `OnlyErrorMessages`: Only error messages

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

### -UseNeighborDP

This parameter is the same as the following setting on the **Download Settings** page of the **Add Phase Wizard** in the console: **Select the deployment option to use when a client uses a distribution point from a neighbor boundary group or the default site boundary group**. Specify the following values:

- `$true`: Download software updates from distribution point and install
- `$false`: Do not install software updates

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

This parameter is the same as the following setting on the **User Experience** page of the **Add Phase Wizard** in the console: **Specify user experience setting for this deployment** with the following values:

- `DisplayAll`: Display in Software Center and show all notifications
- `DisplaySoftwareCenterOnly`: Display in Software Center, and only show notifications for computer restarts
- `HideAll`: Hide in Software Center and all notifications

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

This parameter is the same as the following setting on the **Download Settings** page of the **Add Phase Wizard** in the console: **When software updates are not available on any distribution points in current or neighbor boundary group, client can download and install software updates from distribution points in site default boundary group**. Specify the following values:

- `$true`: Download and install software updates from the distribution points in site default boundary group
- `$false`: Do not install software updates

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

This parameter is the same as the following setting on the **User Experience** page of the **Add Phase Wizard** in the console. Suppress the system restart on the following devices: **Workstations**.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### Microsoft.ConfigurationManager.PhasedDeploymentModel.Phase

## NOTES

## RELATED LINKS
