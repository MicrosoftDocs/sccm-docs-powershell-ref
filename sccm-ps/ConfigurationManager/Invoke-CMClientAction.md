---
description: Sends a notification to client computers to trigger an immediate client action.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/30/2020
online version:
schema: 2.0.0
---

# Invoke-CMClientAction

## SYNOPSIS

Sends a notification to client computers to trigger an immediate client action.

## SYNTAX

### SearchByValueMandatory (Default)
```
Invoke-CMClientAction [-ActionType <ClientActionType>] -Collection <IResultObject>
 [-NotificationType <ClientNotificationType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Invoke-CMClientAction [-ActionType <ClientActionType>] -DeviceName <String>
 [-NotificationType <ClientNotificationType>] [-ParentCollection <IResultObject>]
 [-ParentCollectionId <String>] [-ParentCollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Invoke-CMClientAction [-ActionType <ClientActionType>] -DeviceId <String>
 [-NotificationType <ClientNotificationType>] [-ParentCollection <IResultObject>]
 [-ParentCollectionId <String>] [-ParentCollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceValueMandatory
```
Invoke-CMClientAction [-ActionType <ClientActionType>] -Device <IResultObject>
 [-NotificationType <ClientNotificationType>] [-ParentCollection <IResultObject>]
 [-ParentCollectionId <String>] [-ParentCollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMClientAction [-ActionType <ClientActionType>] -CollectionName <String>
 [-NotificationType <ClientNotificationType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMClientAction [-ActionType <ClientActionType>] -CollectionId <String>
 [-NotificationType <ClientNotificationType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Invoke-CMClientAction** cmdlet sends a notification to client computers to trigger an immediate client action. You can specify one or more client computers, or send a notification to all the computers in a specified device collection.

For more information about these actions, see [Client notification](/mem/configmgr/core/clients/manage/client-notification).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Wake up a device

The following example sends the wake-up action to a device in a specific collection:

```PowerShell
Invoke-CMClientAction -DeviceName "SleepDevice01" -ActionType ClientNotificationWakeUpClientNow -ParentCollectionId $col.CollectionID
```

### Example 2: Request machine policy from a device

This command sends a notification of the type `RequestMachinePolicyNow` to the device named `Computer073`.

```powershell
Invoke-CMClientAction -DeviceName "Computer073" -NotificationType RequestMachinePolicyNow
```

## PARAMETERS

### -ActionType

Specify an action keyword to send to the client. To request machine or user policy, use the **-NotificationType** parameter.

```yaml
Type: ClientActionType
Parameter Sets: (All)
Aliases:
Accepted values: None, EndpointProtectionFullScan, EndpointProtectionQuickScan, EndpointProtectionDownloadDefinition, EndpointProtectionEvaluateSoftwareUpdate, EndpointProtectionExcludeScanPaths, EndpointProtectionAllowThreat, EndpointProtectionRestoreQuarantinedItems, ClientNotificationRequestMachinePolicyNow, ClientNotificationRequestUsersPolicyNow, ClientNotificationRequestDDRNow, ClientNotificationRequestSWInvNow, ClientNotificationRequestHWInvNow, ClientNotificationAppDeplEvalNow, ClientNotificationSUMDeplEvalNow, ClientRequestSUPChangeNow, ClientRequestDHAChangeNow, ClientNotificationRebootMachine, DiagnosticsEnableVerboseLogging, DiagnosticsDisableVerboseLogging, DiagnosticsCollectFiles, EndpointProtectionRestoreWithDeps, ClientNotificationCheckComplianceNow, RequestScriptExecution, RequestCMPivotExecution, ClientNotificationWakeUpClientNow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection

Specify a collection object to target.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: DeviceCollection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId

Specify a collection by ID to target.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: DeviceCollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify a collection by name to target.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: DeviceCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Device

Specify a device object to target.

```yaml
Type: IResultObject
Parameter Sets: SearchByDeviceValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceId

Specify a device by ID to target.

```yaml
Type: String
Parameter Sets: SearchByDeviceIdMandatory
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName

Specify a device by name to target.

```yaml
Type: String
Parameter Sets: SearchByDeviceNameMandatory
Aliases: Name

Required: True
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

### -NotificationType

Request machine or user policy from a client. To trigger all other actions, use the **-ActionType** parameter.

```yaml
Type: ClientNotificationType
Parameter Sets: (All)
Aliases:
Accepted values: RequestMachinePolicyNow, RequestUsersPolicyNow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentCollection

Applies to version 1906 and later. Use this parameter to support waking up a machine.

```yaml
Type: IResultObject
Parameter Sets: SearchByDeviceNameMandatory, SearchByDeviceIdMandatory, SearchByDeviceValueMandatory
Aliases: ParentDeviceCollection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentCollectionId

Applies to version 1906 and later. Use this parameter to support waking up a machine.

```yaml
Type: String
Parameter Sets: SearchByDeviceNameMandatory, SearchByDeviceIdMandatory, SearchByDeviceValueMandatory
Aliases: ParentDeviceCollectionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentCollectionName

Applies to version 1906 and later. Use this parameter to support waking up a machine.

```yaml
Type: String
Parameter Sets: SearchByDeviceNameMandatory, SearchByDeviceIdMandatory, SearchByDeviceValueMandatory
Aliases: ParentDeviceCollectionName

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

Shows what would happen if the cmdlet runs. It doesn't run the cmdlet.

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

Cmdlet aliases: **Invoke-CMClientNotification**

## RELATED LINKS

[Get-CMDevice](Get-CMDevice.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Client notifications](/mem/configmgr/core/clients/manage/client-notification)
