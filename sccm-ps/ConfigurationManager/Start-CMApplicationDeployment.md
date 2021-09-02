---
description: Starts an application deployment in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Start-CMApplicationDeployment
---

# Start-CMApplicationDeployment

## SYNOPSIS
(Deprecated) Starts an application deployment in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Start-CMApplicationDeployment [-ApprovalRequired <Boolean>] [-AvailableDate <DateTime>]
 [-AvailableDateTime <DateTime>] [-AvailableTime <DateTime>] -CollectionName <String> [-Comment <String>]
 [-DeadlineDate <DateTime>] [-DeadlineDateTime <DateTime>] [-DeadlineTime <DateTime>]
 [-DeployAction <DeployActionType>] [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>]
 [-FailParameterValue <Int32>] [-GenerateScomAlertOnFailure <Boolean>] [-InputObject] <IResultObject>
 [-OverrideServiceWindow <Boolean>] [-PassThru] [-PersistOnWriteFilterDevice <Boolean>]
 [-PostponeDate <DateTime>] [-PostponeDateTime <DateTime>] [-PostponeTime <DateTime>] [-PreDeploy <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-SendWakeupPacket <Boolean>] [-SuccessParameterValue <Int32>]
 [-TimeBaseOn <TimeType>] [-UpdateSupersedence <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-UserNotification <UserNotificationType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Start-CMApplicationDeployment [-ApprovalRequired <Boolean>] [-AvailableDate <DateTime>]
 [-AvailableDateTime <DateTime>] [-AvailableTime <DateTime>] -CollectionName <String> [-Comment <String>]
 [-DeadlineDate <DateTime>] [-DeadlineDateTime <DateTime>] [-DeadlineTime <DateTime>]
 [-DeployAction <DeployActionType>] [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>]
 [-FailParameterValue <Int32>] [-GenerateScomAlertOnFailure <Boolean>] [-Id] <Int32>
 [-OverrideServiceWindow <Boolean>] [-PassThru] [-PersistOnWriteFilterDevice <Boolean>]
 [-PostponeDate <DateTime>] [-PostponeDateTime <DateTime>] [-PostponeTime <DateTime>] [-PreDeploy <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-SendWakeupPacket <Boolean>] [-SuccessParameterValue <Int32>]
 [-TimeBaseOn <TimeType>] [-UpdateSupersedence <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-UserNotification <UserNotificationType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Start-CMApplicationDeployment [-ApprovalRequired <Boolean>] [-AvailableDate <DateTime>]
 [-AvailableDateTime <DateTime>] [-AvailableTime <DateTime>] -CollectionName <String> [-Comment <String>]
 [-DeadlineDate <DateTime>] [-DeadlineDateTime <DateTime>] [-DeadlineTime <DateTime>]
 [-DeployAction <DeployActionType>] [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>]
 [-FailParameterValue <Int32>] [-GenerateScomAlertOnFailure <Boolean>] [-Name] <String>
 [-OverrideServiceWindow <Boolean>] [-PassThru] [-PersistOnWriteFilterDevice <Boolean>]
 [-PostponeDate <DateTime>] [-PostponeDateTime <DateTime>] [-PostponeTime <DateTime>] [-PreDeploy <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-SendWakeupPacket <Boolean>] [-SuccessParameterValue <Int32>]
 [-TimeBaseOn <TimeType>] [-UpdateSupersedence <Boolean>] [-UseMeteredNetwork <Boolean>]
 [-UserNotification <UserNotificationType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!IMPORTANT]
> This cmdlet is deprecated. Use [New-CMApplicationDeployment](New-CMApplicationDeployment.md) instead.

The **Start-CMApplicationDeployment** cmdlet starts an application deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Start application deployment
```
PS XYZ:\> Start-CMApplicationDeployment -CollectionName "All Users" -Name "7zip" -AvaliableDate 2012/10/1 -AvaliableTime 12:45 -Comment "test" -DeadlineDate 2013/10/23 -DeadlineTime 21:12 -DeployAction Uninstall -EnableMomAlert $True -FailParameterValue 40 -OverrideServiceWindow $True -PersistOnWriteFilterDevice $False -PostponeDate 2014/2/8 -PostponeTime 11:11 -PreDeploy $True -RaiseMomAlertsOnFailure $True -RebootOutsideServiceWindow $True -SendWakeUpPacket $True -SuccessParameterValue 30 -UseMeteredNetwork $True -UserNotification DisplaySoftwareCenterOnly
```

This command starts an application deployment named 7zip.

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

### -AvailableDate
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: AvailiableDate

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

### -AvailableTime
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: AvailiableTime

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies a target collection to deploy this application.

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

### -Comment
Specifies a comment for the application.

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

### -DeadlineDate
Specifies a day by which to install an application.
Autoinstall performs the installation if the application is not installed.

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

### -DeadlineTime
Specifies a time by which to install an application.
Autoinstall performs the installation if the application is not installed.

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
Specifies an action for a deployment.
Valid values are:

- Install.
Install the application.

- Uninstall.
Uninstall the application.

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
Specifies the purpose of the deployment.

Valid values are:

- Available.
If the target collection is a device collection, the application is available in the software center.
If the target collection is a user collection, the application is available in the catalog web site.

- Required.
Installation occurs when the deadline passes.

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
Indicates whether to enable Operations Manager maintenance mode.

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
Specifies a value that generates a deployment alert when exceeded.

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
Specifies an array of IDs.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an application deployment object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names for the application deployment.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideServiceWindow
Indicates whether an application installation occurs outside of a maintenance window.

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
Indicates whether to commit changes on a Windows Embedded device at deadline or during a maintenance window.
Otherwise, changes are written on the overlay and committed later.

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

### -PostponeDate
Specifies a date after which to create an alert.

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

### -PostponeTime
Specifies a time after which to create an alert.

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
Indicates whether to copy software to a device before installation.
To use this parameter, set the *DeployPurpose* parameter to Required.

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
Indicates whether a computer restarts outside a service window.
A service window is a specified period of time used for computer maintenance and updates.
If this value is $True, any required restart takes place without regard to service windows.
If this value is $False, the computer does not restart outside a service window.

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
Indicates whether to send a wake up packet to computers before the deployment begins.
If this value is $True, Configuration Manager wakes a computer from sleep.
If this value is $False, it does not wake computers from sleep.
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
Specifies a value that the threshold must exceed before an alert is created.

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
Specifies the time zone to use.

Valid values are:

- LocalTime.
Use local time.
- UTC.
Use Coordinated Universal Time (UTC), also known as Greenwich Mean Time.

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
{{ Fill UpdateSupersedence Description }}

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
Indicates whether clients can download content over metered Internet connections after the installation deadline.
Clients may incur additional costs.

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
Specifies user notification types.

Valid values are:

- DisplayAll.
Display in Software Center and show all notifications.

- DisplaySoftwareCenterOnly.
Display in Software Center and only show notifications for computer restarts.

- HideAll.
Do not display in Software Center and do not show notifications.

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

### System.Object
## NOTES

## RELATED LINKS

[Set-CMApplicationDeployment](Set-CMApplicationDeployment.md)
