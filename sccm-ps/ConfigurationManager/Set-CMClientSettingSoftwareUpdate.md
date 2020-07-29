---
description: Sets a client setting software update.
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMClientSettingSoftwareUpdate
---

# Set-CMClientSettingSoftwareUpdate

## SYNOPSIS
Sets a client setting software update.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingSoftwareUpdate [-Enable <Boolean>] [-ScanSchedule <IResultObject>]
 [-DeploymentEvaluationSchedule <IResultObject>] [-BatchingTimeout <Int32>] [-EnforceMandatory <Boolean>]
 [-TimeUnit <BatchingTimeoutType>] [-Office365ManagementType <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-EnableDeltaDownload <Boolean>] [-DeltaDownloadPort <Int32>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingSoftwareUpdate [-Enable <Boolean>] [-ScanSchedule <IResultObject>]
 [-DeploymentEvaluationSchedule <IResultObject>] [-BatchingTimeout <Int32>] [-EnforceMandatory <Boolean>]
 [-TimeUnit <BatchingTimeoutType>] [-Office365ManagementType <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-EnableDeltaDownload <Boolean>] [-DeltaDownloadPort <Int32>] [-DefaultSetting] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingSoftwareUpdate [-Enable <Boolean>] [-ScanSchedule <IResultObject>]
 [-DeploymentEvaluationSchedule <IResultObject>] [-BatchingTimeout <Int32>] [-EnforceMandatory <Boolean>]
 [-TimeUnit <BatchingTimeoutType>] [-Office365ManagementType <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-EnableDeltaDownload <Boolean>] [-DeltaDownloadPort <Int32>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Enable third-party updates in the default client settings

```
PowerShell
Set-CMClientSettingSoftwareUpdate -DefaultSetting -Enable $true -EnableThirdPartyUpdates $true
```

### Example 2: Enable third-party updates in a custom device setting

```
PowerShell
$clientDeviceSettingName = "Dev device settings"
Set-CMClientSettingSoftwareUpdate -Name $clientDeviceSettingName -Enable $true -EnableThirdPartyUpdates $true
```

## PARAMETERS

### -BatchingTimeout
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

### -DefaultSetting
```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeltaDownloadPort
Use this parameter to configure the network port value for the following client setting in the **Software Updates** group: **Port that clients use to receive requests for delta content**. Use the **EnableDeltaDownload** parameter to enable the behavior.

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

### -DeploymentEvaluationSchedule
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

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -Enable
Use this parameter to enable or disable the following client setting in the **Software Updates** group: **Enable software updates on clients**.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableSoftwareUpdatesOnClient

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDeltaDownload

Use this parameter to enable or disable the following client setting in the **Software Updates** group: **Allow clients to download delta content when available**. Use the **DeltaDownloadPort** parameter to configure the network port.

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

### -EnableThirdPartyUpdates
Starting in version 1910, use this parameter to enable or disable the following client setting in the **Software Updates** group: **Enable third party software updates**.

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

### -EnforceMandatory
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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Office365ManagementType
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
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -ScanSchedule
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

### -TimeUnit
```yaml
Type: BatchingTimeoutType
Parameter Sets: (All)
Aliases:
Accepted values: Days, Hours

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
