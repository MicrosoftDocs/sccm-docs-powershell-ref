---
description: Configure client settings for software updates.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
schema: 2.0.0
title: Set-CMClientSettingSoftwareUpdate
---

# Set-CMClientSettingSoftwareUpdate

## SYNOPSIS

Configure client settings for software updates.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingSoftwareUpdate [-BatchingTimeout <Int32>] [-DeltaDownloadPort <Int32>]
 [-DeploymentEvaluationSchedule <IResultObject>] [-Enable <Boolean>] [-EnableDeltaDownload <Boolean>]
 [-EnableDynamicUpdate <Boolean>] [-EnableInstallation <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-EnableWsusCertPinning <Boolean>] [-EnforceMandatory <Boolean>] [-Office365ManagementType <Boolean>]
 [-ScanSchedule <IResultObject>] [-ThreadPriority <ThreadPriorityType>] [-TimeUnit <BatchingTimeoutType>]
 -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingSoftwareUpdate [-BatchingTimeout <Int32>] [-DeltaDownloadPort <Int32>]
 [-DeploymentEvaluationSchedule <IResultObject>] [-Enable <Boolean>] [-EnableDeltaDownload <Boolean>]
 [-EnableDynamicUpdate <Boolean>] [-EnableInstallation <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-EnableWsusCertPinning <Boolean>] [-EnforceMandatory <Boolean>] [-Office365ManagementType <Boolean>]
 [-ScanSchedule <IResultObject>] [-ThreadPriority <ThreadPriorityType>] [-TimeUnit <BatchingTimeoutType>]
 [-DefaultSetting] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingSoftwareUpdate [-BatchingTimeout <Int32>] [-DeltaDownloadPort <Int32>]
 [-DeploymentEvaluationSchedule <IResultObject>] [-Enable <Boolean>] [-EnableDeltaDownload <Boolean>]
 [-EnableDynamicUpdate <Boolean>] [-EnableInstallation <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-EnableWsusCertPinning <Boolean>] [-EnforceMandatory <Boolean>] [-Office365ManagementType <Boolean>]
 [-ScanSchedule <IResultObject>] [-ThreadPriority <ThreadPriorityType>] [-TimeUnit <BatchingTimeoutType>]
 -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure settings in the **Software updates** group of client settings. For more information, see [About client settings: Software updates](/mem/configmgr/core/clients/deploy/about-client-settings#software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Enable third-party updates in the default client settings

```powershell
Set-CMClientSettingSoftwareUpdate -DefaultSetting -Enable $true -EnableThirdPartyUpdates $true
```

### Example 2: Enable third-party updates in a custom device setting

```powershell
$clientDeviceSettingName = "Dev device settings"
Set-CMClientSettingSoftwareUpdate -Name $clientDeviceSettingName -Enable $true -EnableThirdPartyUpdates $true
```

### Example 3: Configure multiple settings

```powershell
Set-CMClientSettingSoftwareUpdate -InputObject $testsetting -Enable $true -ScanSchedule $Sch1 -DeploymentEvaluationSchedule $Sch2 -BatchingTimeout 3 -TimeUnit Days -EnforceMandatory $true -Office365ManagementType $false -EnableThirdPartyUpdates $true -EnableDeltaDownload $true -EnableInstallation $true -ThreadPriority Normal -EnableDynamicUpdate $true
```

## PARAMETERS

### -BatchingTimeout

Specify the period of time for which all pending deployments with a deadline in this time will also be installed. Use this parameter with the **EnforceMandatory** parameter. You can enter a value from 1 to 23 hours, and from 1 to 365 days. By default, this setting is configured for seven days. Use the **TimeUnit** parameter to specify hours or days.

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

Add this parameter to configure software update settings in the default client settings.

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

Use this parameter to configure the network port that clients use to receive requests for delta content. Use the **EnableDeltaDownload** parameter to enable the behavior. The default value is `8005`.

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

Specify how often the software updates client agent reevaluates software updates for installation status on Configuration Manager client computers. To create a new schedule token, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -Enable

Set this parameter to `$true` to enable software updates on clients.

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

Set this parameter to `$true` to allow clients to download delta content when available. To configure the network port, use the **DeltaDownloadPort** parameter.

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

### -EnableDynamicUpdate

Applies to version 2010 and later. Set this parameter to `$true` to enable dynamic update for Windows 10 feature updates. Dynamic update installs language packs, features on demand, drivers, and cumulative updates during Windows setup. It directs the client to download these updates from the internet.

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

### -EnableInstallation

Applies to version 2010 and later. Set this parameter to `$true` to enable installation of software updates in the "All deployments" maintenance window when the "Software Update" maintenance window is available.

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

Set this parameter to `$true` to enable third-party software updates.

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

### -EnableWsusCertPinning

Applies to version 2107 and later. Set this parameter to `$true` to enforce TLS certificate pinning for Windows Update client for detecting updates.

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

When any software update deployment deadline is reached, install all other software update deployments with deadline coming within a specified period of time. Use the **BatchingTimeout** parameter to specify the period of time.

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

This cmdlet adds the software update settings to the client settings object that you specify with this parameter. To get this object, use the [Get-CMClientSetting](Get-CMClientSetting.md) cmdlet.

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

This cmdlet adds the software update settings to the client settings object that this parameter names.

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

Set this parameter to `$true` to enable management of the Microsoft 365 Apps client agent and installation settings.

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

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

Specify how often the software updates client agent starts a compliance assessment scan. This scan determines the state for software updates on the client. To create a new schedule token, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -ThreadPriority

Applies to version 2010 and later. Specify a thread priority for Windows 10 feature updates.

- `Normal`: Windows Setup uses more system resources and updates faster. It uses more processor time, so the total installation time is shorter, but the user's outage is longer. This value is the default.

- `Low`: You can continue to work on the device while it downloads and updates in the background. The total installation time is longer, but the user's outage is shorter. You may need to increase the update max run time to avoid a time-out when you use this option.

```yaml
Type: ThreadPriorityType
Parameter Sets: (All)
Aliases:
Accepted values: Normal, Low

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeUnit

Use with the **BatchingTimeout** parameter to specify the period of time for which all pending deployments with a deadline in this time will also be installed.

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

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

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

[Get-CMClientSetting](Get-CMClientSetting.md)

[Remove-CMClientSetting](Remove-CMClientSetting.md)

[New-CMSchedule](New-CMSchedule.md)

[About client settings: Software updates](/mem/configmgr/core/clients/deploy/about-client-settings#software-updates)
