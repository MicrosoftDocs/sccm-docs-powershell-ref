---
description: Create an application deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/23/2020
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

The **New-CMApplicationDeployment** cmdlet creates an application deployment. For more information, see [Deploy applications with Configuration Manager](/mem/configmgr/apps/deploy-use/deploy-applications).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Install an application

This command creates a new deployment for **Visual Studio 2019** to the collection **Developers Workstation**. It installs the app, and is required. Both the available date and deadline are the same time in the past, so as soon as the client receives this policy, it installs the app.

```powershell
New-CMApplicationDeployment -Name "Visual Studio 2019" -AvailableDateTime '01/01/2020 00:00:00' -CollectionName 'Developers Workstation' -DeadlineDateTime '01/01/2020 00:00:00' -DeployAction Install -DeployPurpose Required
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

If you set this parameter to `$true`, an administrator must approve a request for this application on the device.

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

Specify a **DateTime** object for when this deployment is _available_. To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

Use **DeadlineDateTime** to specify the deployment assignment, or _deadline_.

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

Specify a collection object to which the application is deployed. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify the ID of the collection to which this application is deployed. For example, `"SMS00004"`.

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

Specify the name of the collection to which this application is deployed.

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

Specify an optional comment for this deployment.

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

### -DeadlineDateTime

Specify a **DateTime** object for when this deployment is assigned, also known as the _deadline_. To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

Use **-AvailableDateTime** to specify when the deployment is _available_.

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

Specify the deployment action, either to install or uninstall the application. If competing deployments target the same device, the **Install** action takes priority.

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

Specify the deployment purpose:

- `Available`: The user sees the application in Software Center. They can install it on demand.

- `Required`: The client automatically installs the app according to the schedule that you set. If the application isn't hidden, a user can track its deployment status. They can also use Software Center to install the application before the deadline.

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

Add this parameter to not automatically distribute content for dependent apps.

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

### -DistributeCollectionName

The site distributes content to the distribution points that are associated with this collection name.

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

Add this parameter if you need to distribute the app content first.

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

To distribute the application content, specify the name of a distribution point group.

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

To distribute the application content, specify the name of a distribution point.

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

Set this parameter to `$true` to enable System Center Operations Manager maintenance mode for this deployment.

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

Set this parameter to `$true` to enable delayed enforcement.

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

Specifies the percentage of failed application installation that causes an alert.
Specify an integer from 1 through 100.
To enable this alert, set the **CreatAlertBaseOnPercentFailure** parameter to `$True`.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

Indicates whether to create an Operations Manager alert if a client fails to install the application.

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

Specify the ID of the application to deploy.

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

Specify an application object to deploy. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

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

Specify the name of the application to deploy.

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

Indicates whether the deployment takes place even if scheduled outside of a maintenance window.
A maintenance window is a specified period of time used for computer maintenance and updates.
If this value is `$True`, Configuration Manager deploys the application even if the scheduled time falls outside the maintenance window.
If this value is `$False`, Configuration Manager doesn't deploy the application outside the window. It waits until it can deploy in an available window.

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

Indicates whether to enable write filters for embedded devices.
For a value of `$True`, the device commits changes during a maintenance window. This action requires a restart.
For a value of `$False`, the device saves changes in an overlay and commits them later.

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

When you set **CreateAlertBaseOnPercentSuccess** to `$true`, use this parameter to specify a **DateTime** object. Configuration Manager creates a deployment alert when the threshold is lower than the **SuccessParameterValue** after this date.

To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

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

Indicates whether to pre-deploy the application to the primary device of the user.

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

Indicates whether a computer restarts outside a maintenance window.
A maintenance window is a specified period of time used for computer maintenance and updates.
If this value is `$True`, any required restart takes place without regard to maintenance windows.
If this value is `$False`, the computer doesn't restart outside a maintenance window.

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

When required software is available on the client, set this parameter to `$true` to replace the default toast notifications with a dialog window. It's false by default. For more information, see [Replace toast notifications with dialog window](/mem/configmgr/apps/plan-design/plan-for-software-center#bkmk_impact).

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

Indicates whether to send a wake-up packet to computers before the deployment begins.
If this value is `$True`, Configuration Manager attempts to wake a computer from sleep.
If this value is `$False`, it doesn't wake computers from sleep.
For computers to wake, you must first configure Wake On LAN.

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

Add this parameter to create a deployment simulation. For more information, see [Simulate application deployments with Configuration Manager](/mem/configmgr/apps/deploy-use/simulate-application-deployments).

To start the simulation, use the [Start-CMApplicationDeploymentSimulation](Start-CMApplicationDeploymentSimulation.md) cmdlet.

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

Specifies the percentage of successful application installation that causes an alert.
Specify an integer from 0 through 99.
To enable this alert, set the **CreateAlertBaseOnPercentSuccess** parameter as `$True`.

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

Specifies which time zone to use:

- `LocalTime`: Use local time.
- `UTC`: Use Coordinated Universal Time (UTC).

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

For an available deployment, use this parameter to specify the installation deadline to upgrade users or devices that have the superseded application installed. Use **DeadlineDateTime** to specify a specific time, otherwise it's as soon as possible after the **AvailableDateTime**.

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

Indicates whether to allow clients to download content over a metered internet connection after the deadline, which may incur extra expense.

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

Specifies the type of user notification.

- `DisplayAll`: Display in Software Center and show all notifications.
- `DisplaySoftwareCenterOnly`: Display in Software Center, and only show notifications of computer restarts.
- `HideAll`: Hide in Software Center and all notifications.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Get-CMApplicationDeployment](Get-CMApplicationDeployment.md)

[Remove-CMApplicationDeployment](Remove-CMApplicationDeployment.md)

[Set-CMApplicationDeployment](Set-CMApplicationDeployment.md)

[Start-CMApplicationDeployment](Start-CMApplicationDeployment.md)

[Start-CMApplicationDeploymentSimulation](Start-CMApplicationDeploymentSimulation.md)

[Deploy applications with Configuration Manager](/mem/configmgr/apps/deploy-use/deploy-applications)
