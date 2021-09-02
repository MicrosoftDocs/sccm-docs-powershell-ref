---
description: Configure an application deployment
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/28/2021
schema: 2.0.0
title: Set-CMApplicationDeployment
---

# Set-CMApplicationDeployment

## SYNOPSIS

Configure an application deployment

## SYNTAX

### SetApplicationDeploymentByValueMandatory (Default)
```
Set-CMApplicationDeployment [-AllowRepairApp <Boolean>] [-AutoCloseExecutable <Boolean>]
 [-AvailableDateTime <DateTime>] [-Comment <String>] [-CreateAlertBaseOnPercentFailure <Boolean>]
 [-CreateAlertBaseOnPercentSuccess <Boolean>] [-DeadlineDateTime <DateTime>] [-EnableMomAlert <Boolean>]
 [-EnableSoftDeadline <Boolean>] [-FailParameterValue <Int32>] -InputObject <IResultObject>
 [-OverrideServiceWindow <Boolean>] [-PersistOnWriteFilterDevice <Boolean>] [-PostponeDateTime <DateTime>]
 [-PreDeploy <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-ReplaceToastNotificationWithDialog <Boolean>] [-RequireApproval <Boolean>] [-SendWakeUpPacket <Boolean>]
 [-SuccessParameterValue <Int32>] [-TimeBaseOn <TimeType>] [-UseMeteredNetwork <Boolean>]
 [-UserNotification <UserNotificationType>] [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetApplicationDeploymentByIdMandatory
```
Set-CMApplicationDeployment [-AllowRepairApp <Boolean>] -ApplicationId <String>
 [-AutoCloseExecutable <Boolean>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-CreateAlertBaseOnPercentFailure <Boolean>] [-CreateAlertBaseOnPercentSuccess <Boolean>]
 [-DeadlineDateTime <DateTime>] [-EnableMomAlert <Boolean>] [-EnableSoftDeadline <Boolean>]
 [-FailParameterValue <Int32>] [-OverrideServiceWindow <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-PostponeDateTime <DateTime>] [-PreDeploy <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-ReplaceToastNotificationWithDialog <Boolean>]
 [-RequireApproval <Boolean>] [-SendWakeUpPacket <Boolean>] [-SuccessParameterValue <Int32>]
 [-TimeBaseOn <TimeType>] [-UseMeteredNetwork <Boolean>] [-UserNotification <UserNotificationType>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetApplicationDeploymentByNameMandatory
```
Set-CMApplicationDeployment [-AllowRepairApp <Boolean>] -ApplicationName <String>
 [-AutoCloseExecutable <Boolean>] [-AvailableDateTime <DateTime>] [-Comment <String>]
 [-CreateAlertBaseOnPercentFailure <Boolean>] [-CreateAlertBaseOnPercentSuccess <Boolean>]
 [-DeadlineDateTime <DateTime>] [-EnableMomAlert <Boolean>] [-EnableSoftDeadline <Boolean>]
 [-FailParameterValue <Int32>] [-OverrideServiceWindow <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-PostponeDateTime <DateTime>] [-PreDeploy <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-ReplaceToastNotificationWithDialog <Boolean>]
 [-RequireApproval <Boolean>] [-SendWakeUpPacket <Boolean>] [-SuccessParameterValue <Int32>]
 [-TimeBaseOn <TimeType>] [-UseMeteredNetwork <Boolean>] [-UserNotification <UserNotificationType>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMApplicationDeployment** cmdlet modifies the properties of an application deployment in Configuration Manager. For more information, see [Deploy applications with Configuration Manager](/mem/configmgr/apps/deploy-use/deploy-applications).

To specify an application deployment to modify, specify the collection name and the application. You can specify an application by name or ID. You can also use the [Get-CMApplication](Get-CMApplication.md) cmdlet to get an application to modify.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify availability and deadline for an application deployment

```PowerShell
Set-CMApplicationDeployment -ApplicationName "Track System 2011" -CollectionName "All Users" -AvailableDateTime (Get-Date) -DeadlineDateTime $(Get-Date).AddDays(30)
```

This command modifies an application deployment for an application named **Track System 2011** for a collection named **All Users**. The command specifies the current date for when the application is available. It also configures the deployment deadline for 30 days in the future.

## PARAMETERS

### -AllowRepairApp

Use this parameter to configure the repair application option when creating a deployment for an application.

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

### -ApplicationId
Specifies the ID of an application.

```yaml
Type: String
Parameter Sets: SetApplicationDeploymentByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies the name of an application.

```yaml
Type: String
Parameter Sets: SetApplicationDeploymentByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoCloseExecutable

Starting in version 2107, set this parameter to `$true` to enable the application deployment setting for install behaviors. Then use the [Add-CMDeploymentTypeInstallBehavior](Add-CMDeploymentTypeInstallBehavior.md) cmdlet to add an executable file to check isn't running for the install to succeed.

Set this parameter to `$false` to disable this option in the following situations:

- When you use the [Remove-CMDeploymentTypeInstallBehavior](Remove-CMDeploymentTypeInstallBehavior.md) cmdlet to remove all executable files
- You don't want the deployment to check for running executables.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AutoCloseExeOnInstallBehavior

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

Specify the ID of the collection to which the application is deployed. For example, `"SMS00004"`.

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

Specify the name of the collection to which the application is deployed.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Comment

Specifies an optional comment for the deployment.

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

### -CreateAlertBaseOnPercentFailure

Indicates whether to create an alert for a percentage of the applications that fail to deploy.
To specify the percentage value, use the **FailParameterValue** parameter.

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

### -CreateAlertBaseOnPercentSuccess

Indicates whether to create an alert for a percentage of the applications that deploy successfully.
To specify the percentage value, use the **SuccessParameterValue** parameter.

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

### -DeadlineDateTime

Specify a **DateTime** object for when this deployment is assigned, also known as the _deadline_. To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

Use **-AvailableDateTime** to specify when the deployment is _available_.

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

### -InputObject

Specify an application deployment object to configure. To get this object, use the [Get-CMApplicationDeployment](Get-CMApplicationDeployment.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetApplicationDeploymentByValueMandatory
Aliases: Application, DeploymentSummary, Assignment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -RaiseMomAlertsOnFailure

Indicates whether to create an Operations Manager alert if a client fails to install the application.

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

### -RequireApproval

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

### -SendWakeUpPacket

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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_ApplicationAssignment
## NOTES

For more information on this return object and its properties, see [SMS_ApplicationAssignment server WMI class](/mem/configmgr/develop/reference/apps/sms_applicationassignment-server-wmi-class).

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Get-CMApplicationDeployment](Get-CMApplicationDeployment.md)

[New-CMApplicationDeployment](New-CMApplicationDeployment.md)

[Remove-CMApplicationDeployment](Remove-CMApplicationDeployment.md)

[Deploy applications with Configuration Manager](/mem/configmgr/apps/deploy-use/deploy-applications)
