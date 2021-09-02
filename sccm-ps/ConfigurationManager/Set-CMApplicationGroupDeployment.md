---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Set-CMApplicationGroupDeployment

## SYNOPSIS

Configure the deployment of an application group.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMApplicationGroupDeployment [-Comment <String>] [-DeadlineDateTime <DateTime>] [-TimeBaseOn <TimeType>]
 -InputObject <IResultObject> [-AvailableDateTime <DateTime>] [-UserNotification <UserNotificationType>]
 [-EnableMomAlert <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>] [-OverrideServiceWindow <Boolean>]
 [-PersistOnWriteFilterDevice <Boolean>] [-RebootOutsideServiceWindow <Boolean>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByIdMandatory
```
Set-CMApplicationGroupDeployment -ApplicationGroudId <String> [-Comment <String>]
 [-DeadlineDateTime <DateTime>] [-TimeBaseOn <TimeType>] [-AvailableDateTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-EnableMomAlert <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMApplicationGroupDeployment -ApplicationGroupName <String> [-Comment <String>]
 [-DeadlineDateTime <DateTime>] [-TimeBaseOn <TimeType>] [-AvailableDateTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-EnableMomAlert <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-PassThru] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Configure the deployment of an application group. An app group contains multiple applications, and users see the group in Software Center as a single entity. For more information, see [Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
$collection = Get-CMCollection -Name "co1"

Set-CMApplicationGroupDeployment -ApplicationGroupName "appGroupTest" -Collection $collection -Comment "modify comment"
```

## PARAMETERS

### -ApplicationGroudId

Specify the ID of the app group to configure.

```yaml
Type: String
Parameter Sets: SetByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationGroupName

Specify the name of the app group to configure.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
Aliases:

Required: True
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

Specify a collection object as the target for this app group deployment. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify a collection ID as the target for this app group deployment.

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

Specify a collection name as the target for this app group deployment.

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

Specify an optional comment for the app group deployment.

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

Specify an object for the app group. To get this object, use the [Get-CMApplicationGroup](Get-CMApplicationGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases: ApplicationGroup, DeploymentSummary, ApplicationGroupAssignment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OverrideServiceWindow

Set this parameter to `$true` to install the app group outside a maintenance window.

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

Use this parameter to handle write filters for Windows Embedded devices. If you set it to `$true`, the device commits changes at the deadline or during a maintenance window. This action requires a restart. If you set it to `$false`, the device saves changes to the temporary overlay and commits them later.

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

Set this parameter to `$true` to generate a System Center Operations Manager alert when the deployment fails.

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

Set this parameter to `$true` to allow the device to restart outside a maintenance window.

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

### -TimeBaseOn

Specify which time zone to use:

- `LocalTime`: Use the local time of the device.
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

### -UserNotification

Use this parameter to specify the user experience for this deployment:

- `DisplayAll`: Display in Software Center and show all notifications
- `DisplaySoftwareCenterOnly`: Display in Software Center, and only show notifications of computer restarts.
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

### IResultObject#SMS_ApplicationGroupAssignment
### IResultObject#SMS_DeploymentSummary
## NOTES

This cmdlet returns the SMS_ApplicationGroupAssignment WMI class object.

## RELATED LINKS

[Get-CMApplicationGroupDeployment](Get-CMApplicationGroupDeployment.md)

[New-CMApplicationGroupDeployment](New-CMApplicationGroupDeployment.md)

[Remove-CMApplicationGroupDeployment](Remove-CMApplicationGroupDeployment.md)

[Get-CMApplicationGroup](Get-CMApplicationGroup.md)

[Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups)
