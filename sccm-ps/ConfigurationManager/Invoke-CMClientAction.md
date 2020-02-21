---
external help file: AdminUI.PS.Collections.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Invoke-CMClientAction

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByDeviceValueMandatory (Default)
```
Invoke-CMClientAction -Device <IResultObject> [-NotificationType <ClientNotificationType>]
 [-ActionType <ClientActionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Invoke-CMClientAction -DeviceName <String> [-NotificationType <ClientNotificationType>]
 [-ActionType <ClientActionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Invoke-CMClientAction -DeviceId <String> [-NotificationType <ClientNotificationType>]
 [-ActionType <ClientActionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMClientAction -CollectionName <String> [-NotificationType <ClientNotificationType>]
 [-ActionType <ClientActionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMClientAction -CollectionId <String> [-NotificationType <ClientNotificationType>]
 [-ActionType <ClientActionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMClientAction -Collection <IResultObject> [-NotificationType <ClientNotificationType>]
 [-ActionType <ClientActionType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -ActionType
{{ Fill ActionType Description }}

```yaml
Type: ClientActionType
Parameter Sets: (All)
Aliases:
Accepted values: None, EndpointProtectionFullScan, EndpointProtectionQuickScan, EndpointProtectionDownloadDefinition, EndpointProtectionEvaluateSoftwareUpdate, EndpointProtectionExcludeScanPaths, EndpointProtectionAllowThreat, EndpointProtectionRestoreQuarantinedItems, ClientNotificationRequestMachinePolicyNow, ClientNotificationRequestUsersPolicyNow, ClientNotificationRequestDDRNow, ClientNotificationRequestSWInvNow, ClientNotificationRequestHWInvNow, ClientNotificationAppDeplEvalNow, ClientNotificationSUMDeplEvalNow, ClientRequestSUPChangeNow, ClientRequestDHAChangeNow, ClientNotificationRebootMachine, EndpointProtectionRestoreWithDeps, ClientNotificationCheckComplianceNow, RequestScriptExecution, ClientNotificationWakeUpClientNow

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
Parameter Sets: SearchByValueMandatory
Aliases: DeviceCollection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId
{{ Fill CollectionId Description }}

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
{{ Fill CollectionName Description }}

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

### -Device
{{ Fill Device Description }}

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
{{ Fill DeviceId Description }}

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
{{ Fill DeviceName Description }}

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

### -NotificationType
{{ Fill NotificationType Description }}

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
