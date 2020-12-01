---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
online version:
schema: 2.0.0
---

# Set-CMSoftwareUpdatePhase

## SYNOPSIS

Use this cmdlet to configure a deployment phase for a software update.

## SYNTAX

### SearchByPhasedDeployment
```
Set-CMSoftwareUpdatePhase [-AlertDelta <Int32>] [-AlertThresholdPercentage <Int32>] [-AlertUnit <TimeUnitType>]
 [-AllowMeteredConnection <Boolean>] [-AllowSystemRestart <Boolean>] [-AllowWumuFallback <Boolean>]
 [-DisableScomAlert <Boolean>] [-EnableAlert <Boolean>] [-EnableWakeOnLan <Boolean>]
 [-GenerateScomAlertOnFailure <Boolean>] [-PhaseDescription <String>] [-RequirePostRebootFullScan <Boolean>]
 [-ServerRestartSuppression <Boolean>] [-SoftwareInstallation <Boolean>]
 [-StateMessageVerbosity <VerbosityLevelType>] [-UseNeighborDP <Boolean>]
 [-UserNotificationOption <UserNotificationType>] [-UseSiteDefaultDP <Boolean>]
 [-WorkstationRestartSuppression <Boolean>] [-WriteFilterCommit <Boolean>]
 [-BeginCondition <BeginConditionType>] [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>]
 [-DaysAfterPreviousPhaseSuccess <Int32>] [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>]
 [-InstallationChoice <InstallationChoiceType>] [-MovePhase <ReorderType>] [-MoveToOrder <Int32>]
 [-NewCollection <IResultObject>] [-NewCollectionId <String>] [-NewCollectionName <String>]
 [-NewPhaseName <String>] [-ThrottlingDays <Int32>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-Id <String>] [-InputObject] <IResultObject> [-Name <String>] [-Order <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByPhasedDeploymentId
```
Set-CMSoftwareUpdatePhase [-AlertDelta <Int32>] [-AlertThresholdPercentage <Int32>] [-AlertUnit <TimeUnitType>]
 [-AllowMeteredConnection <Boolean>] [-AllowSystemRestart <Boolean>] [-AllowWumuFallback <Boolean>]
 [-DisableScomAlert <Boolean>] [-EnableAlert <Boolean>] [-EnableWakeOnLan <Boolean>]
 [-GenerateScomAlertOnFailure <Boolean>] [-PhaseDescription <String>] [-RequirePostRebootFullScan <Boolean>]
 [-ServerRestartSuppression <Boolean>] [-SoftwareInstallation <Boolean>]
 [-StateMessageVerbosity <VerbosityLevelType>] [-UseNeighborDP <Boolean>]
 [-UserNotificationOption <UserNotificationType>] [-UseSiteDefaultDP <Boolean>]
 [-WorkstationRestartSuppression <Boolean>] [-WriteFilterCommit <Boolean>]
 [-BeginCondition <BeginConditionType>] [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>]
 [-DaysAfterPreviousPhaseSuccess <Int32>] [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>]
 [-InstallationChoice <InstallationChoiceType>] [-MovePhase <ReorderType>] [-MoveToOrder <Int32>]
 [-NewCollection <IResultObject>] [-NewCollectionId <String>] [-NewCollectionName <String>]
 [-NewPhaseName <String>] [-ThrottlingDays <Int32>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-Id <String>] [-Name <String>] [-Order <Int32>] [-PhasedDeploymentId] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByPhasedDeploymentName
```
Set-CMSoftwareUpdatePhase [-AlertDelta <Int32>] [-AlertThresholdPercentage <Int32>] [-AlertUnit <TimeUnitType>]
 [-AllowMeteredConnection <Boolean>] [-AllowSystemRestart <Boolean>] [-AllowWumuFallback <Boolean>]
 [-DisableScomAlert <Boolean>] [-EnableAlert <Boolean>] [-EnableWakeOnLan <Boolean>]
 [-GenerateScomAlertOnFailure <Boolean>] [-PhaseDescription <String>] [-RequirePostRebootFullScan <Boolean>]
 [-ServerRestartSuppression <Boolean>] [-SoftwareInstallation <Boolean>]
 [-StateMessageVerbosity <VerbosityLevelType>] [-UseNeighborDP <Boolean>]
 [-UserNotificationOption <UserNotificationType>] [-UseSiteDefaultDP <Boolean>]
 [-WorkstationRestartSuppression <Boolean>] [-WriteFilterCommit <Boolean>]
 [-BeginCondition <BeginConditionType>] [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>]
 [-DaysAfterPreviousPhaseSuccess <Int32>] [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>]
 [-InstallationChoice <InstallationChoiceType>] [-MovePhase <ReorderType>] [-MoveToOrder <Int32>]
 [-NewCollection <IResultObject>] [-NewCollectionId <String>] [-NewCollectionName <String>]
 [-NewPhaseName <String>] [-ThrottlingDays <Int32>] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-Id <String>] [-Name <String>] [-Order <Int32>] [-PhasedDeploymentName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Applies to version 2006 and later. Use this cmdlet to configure a deployment phase for a software update. For more information, see [Create phased deployments](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence).

## EXAMPLES

### Example 1: Change the collection

This example changes the collection for the second phase in the software update phased deployment passed through on the command line.

```powershell
$phasedDeployment = Get-CMSoftwareUpdatePhasedDeployment -Name "myPhasedDeployment"

$phasedDeployment | Set-CMSoftwareUpdatePhase -Order 2 -NewCollectionId "XYZ00227"
```

### Example 2: Move a phase up

This example moves a phase up in the order. It selects the phased deployment by its ID, and selects the phase by the associated collection ID.

```powershell
Set-CMSoftwareUpdatePhase -PhasedDeploymentId "0bc464d9-e7dd-44c1-a157-3f8be6a79c03" -CollectionId "XYZ00227" -MovePhase MoveUp
```

### Example 3: Configure phase settings

This example changes the configuration settings for the selected phase.

```powershell
Set-CMSoftwareUpdatePhase -PhasedDeploymentName "myPhasedDeployment" -Name "phase1" -UserNotification HideAll -SoftwareInstallation $true -AllowSystemRestart $true -WriteFilterCommit $false -EnableWakeOnLan $true -PhaseDescription "this is phase 1" -StateMessageVerbosity AllMessages -ServerRestartSuppression $true -WorkstationRestartSuppression $true -RequirePostRebootFullScan $true -EnableAlert $true -AlertThresholdPercentage 90 -AlertDelta 12 -AlertUnit Hours -DisableSCOMAlert $true -GenerateSCOMAlertOnFailure $true -UseNeighborDP $true -UseSiteDefaultDP $true -AllowWUMUFallback $true -AllowMeteredConnection $true -CriteriaOption Compliance -CriteriaValue 90 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 3 -ThrottlingDays 5 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 12
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

### -AllowWumuFallback

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
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

Specify the target collection by ID.

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

Specify the target collection by name.

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

### -DisableScomAlert

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

### -GenerateScomAlertOnFailure

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

### -Id

Specify the ID of the phase to configure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PhaseId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a phased deployment object that includes the phase to configure.

```yaml
Type: IResultObject
Parameter Sets: SearchByPhasedDeployment
Aliases: PhasedDeployment

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### -MovePhase

Change the order for the selected phase. You can move it up one, move it down one, or move to a specific index. If you specify `MoveToOrder`, use the **-MoveToOrder** parameter to set the specific index.

```yaml
Type: ReorderType
Parameter Sets: (All)
Aliases:
Accepted values: MoveUp, MoveDown, MoveToOrder

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveToOrder

When you set the **-MovePhase** parameter to `MoveToOrder`, use this parameter to set the specific index.

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

### -Name

Specify the name of the phase to configure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PhaseName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewCollection

Specify a collection object to use as the new target for the selected phase.

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

### -NewCollectionId

Specify a collection by ID to use as the new target for the selected phase.

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

### -NewCollectionName

Specify a collection by name to use as the new target for the selected phase.

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

### -NewPhaseName

Use this parameter to rename the selected phase.

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

### -Order

Specify the index of the phase to configure.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PhaseOrder

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

### -PhasedDeploymentId

Select the phased deployment by ID. Then use other parameters to select the specific phase in that deployment.

```yaml
Type: String
Parameter Sets: SearchByPhasedDeploymentId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PhasedDeploymentName

Select the phased deployment by name. Then use other parameters to select the specific phase in that deployment.

```yaml
Type: String
Parameter Sets: SearchByPhasedDeploymentName
Aliases:

Required: True
Position: 0
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_PhasedDeployment

## NOTES

## RELATED LINKS

[Get-CMPhase](Get-CMPhase.md)

[New-CMSoftwareUpdatePhase](New-CMSoftwareUpdatePhase.md)

[Get-CMSoftwareUpdatePhasedDeployment](Get-CMSoftwareUpdatePhasedDeployment.md)

[New-CMSoftwareUpdateAutoPhasedDeployment](New-CMSoftwareUpdateAutoPhasedDeployment.md)

[New-CMSoftwareUpdateManualPhasedDeployment](New-CMSoftwareUpdateManualPhasedDeployment.md)

[Remove-CMSoftwareUpdatePhasedDeployment](Remove-CMSoftwareUpdatePhasedDeployment.md)

[Set-CMSoftwareUpdatePhasedDeployment](Set-CMSoftwareUpdatePhase.md)

[Get-CMPhasedDeploymentStatus](Get-CMPhasedDeploymentStatus.md)

[Move-CMPhasedDeploymentToNext](Move-CMPhasedDeploymentToNext.md)

[Resume-CMPhasedDeployment](Resume-CMPhasedDeployment.md)

[Suspend-CMPhasedDeployment](Suspend-CMPhasedDeployment.md)

[Create phased deployments](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence)
