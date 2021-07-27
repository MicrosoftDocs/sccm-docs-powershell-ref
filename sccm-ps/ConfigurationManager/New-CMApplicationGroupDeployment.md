---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# New-CMApplicationGroupDeployment

## SYNOPSIS

Create a deployment for an application group.

## SYNTAX

### SearchByValueMandatory (Default)
```
New-CMApplicationGroupDeployment [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>]
 [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>] [-GenerateScomAlertOnFailure <Boolean>]
 [-InputObject] <IResultObject> [-OverrideServiceWindow <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>]
 [-DistributeContent] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-AvailableDateTime <DateTime>] [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMApplicationGroupDeployment [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>]
 [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>] [-GenerateScomAlertOnFailure <Boolean>]
 [-Id] <Int32> [-OverrideServiceWindow <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>]
 [-DistributeContent] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-AvailableDateTime <DateTime>] [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMApplicationGroupDeployment [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>]
 [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>] [-GenerateScomAlertOnFailure <Boolean>]
 [-Name] <String> [-OverrideServiceWindow <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>]
 [-DistributeContent] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-AvailableDateTime <DateTime>] [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Create a deployment for an application group. An app group contains multiple applications, and users see the group in Software Center as a single entity. For more information, see [Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups).

Before you can deploy an app group, you need to create it. Then you can deploy it to a user or device collection as a single deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
$collection = Get-CMCollection -Name "co1"

$distributionPointName = "dp1.contoso.com"

New-CMApplicationGroupDeployment -Id 16777536 -Collection $collection -DistributionPointName $distributionPointName -DistributeContent
```

## PARAMETERS

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
Aliases: SupersedenceDeadlineDateTime

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeployAction

Specify whether this deployment is to install or uninstall the app group.

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

Specify whether this deployment is available for users to install, or it's required to install at the deadline.

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

Add this parameter to distribute the app group content when you create this deployment. Clients can't install the applications until you distribute content to distribution points that the clients can access.

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

The site distributes content to this distribution point group.

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

The site distributes content to this distribution point.

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

Set this parameter to `$true` to generate a System Center Operations Manager alert when the deployment fails.

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

Specify the ID of the application group to deploy.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID, ApplicationGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for the app group. To get this object, use the [Get-CMApplicationGroup](Get-CMApplicationGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ApplicationGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify a name for this app group deployment.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName, ApplicationGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### -SendWakeupPacket

Indicates whether to send a wake-up packet to computers before the deployment begins. If this value is `$True`, Configuration Manager wakes a computer from sleep. If this value is `$False`, it doesn't wake computers from sleep. For computers to wake, first configure Wake On LAN.

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

### -UseMeteredNetwork

Indicates whether to allow clients on a metered internet connection to download content after the installation deadline, which might incur additional costs.

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
## NOTES

This cmdlet returns the SMS_ApplicationGroupAssignment WMI class object.

## RELATED LINKS

[Get-CMApplicationGroupDeployment](Get-CMApplicationGroupDeployment.md)

[Remove-CMApplicationGroupDeployment](Remove-CMApplicationGroupDeployment.md)

[Set-CMApplicationGroupDeployment](Set-CMApplicationGroupDeployment.md)

[Get-CMApplicationGroup](Get-CMApplicationGroup.md)

[Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups)
