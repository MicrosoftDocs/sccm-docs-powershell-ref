---
description: Change client settings for Configuration Manager devices and users.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: Set-CMClientSetting
---

# Set-CMClientSetting

## SYNOPSIS

Change client settings for Configuration Manager devices and users.

## SYNTAX

### SetByName (Default)
```
Set-CMClientSetting [-Description <String>] -Name <String> [-NewName <String>] [-PassThru]
 [-Priority <PriorityChangeType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRemoteToolsSettingsByName
```
Set-CMClientSetting [-AccessLevel <AccessLevelType>] [-AllowClientChange <Boolean>]
 [-AllowPermittedViewer <Boolean>] [-AllowRemoteControlOfUnattendedComputer <Boolean>]
 [-AudibleSignal <AudibleSignalType>] [-FirewallExceptionProfile <FirewallExceptionProfileType[]>]
 [-GrantRemoteControlPermissionToLocalAdministrator <Boolean>] [-ManageRemoteDesktopSetting <Boolean>]
 [-ManageSolicitedRemoteAssistance <Boolean>] [-ManageUnsolicitedRemoteAssistance <Boolean>] -Name <String>
 [-PassThru] [-PermittedViewer <String[]>] [-PromptUserForPermission <Boolean>]
 [-RemoteAssistanceAccessLevel <RemoteAssistanceAccessLevelType>] [-RemoteControl]
 [-RequireAuthentication <Boolean>] [-ShowNotificationIconOnTaskbar <Boolean>]
 [-ShowSessionConnectionBar <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetComputerAgentSettingsByName
```
Set-CMClientSetting [-AddPortalToTrustedSiteList <Boolean>] [-AllowPortalToHaveElevatedTrust <Boolean>]
 [-ApplicationCatalogWebsitePointServerName <String>] [-BrandingTitle <String>] [-ComputerAgent]
 [-DisplayNewProgramNotification <Boolean>]
 [-EnableThirdPartyOrchestration <EnableThirdPartyOrchestrationType>] [-FinalReminderMins <Int32>]
 [-InitialReminderHours <Int32>] [-InstallRestriction <InstallRestrictionType>] [-InterimReminderHours <Int32>]
 -Name <String> [-PassThru] [-PortalUrl <String>] [-PowerShellExecutionPolicy <PowerShellExecutionPolicyType>]
 [-SelectApplicationCatalogWebsitePoint <ApplicationCatalogWebsitePointType>]
 [-SuspendBitLocker <SuspendBitLockerType>] [-UseNewSoftwareCenter <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCloudSettingsByName
```
Set-CMClientSetting [-AllowCloudDistributionPoint <Boolean>] [-CloudService] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetUserDeviceAffinitySettingsByName
```
Set-CMClientSetting [-AllowUserAffinity <Boolean>] [-AutoApproveAffinity <Boolean>]
 [-LogOnThresholdMins <Int32>] -Name <String> [-PassThru] [-UsageThresholdDays <Int32>] [-UserDeviceAffinity]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetPowerManagementSettingsByName
```
Set-CMClientSetting [-AllowUserToOptOutFromPowerPlan <Boolean>] [-Enable <Boolean>]
 [-EnableWakeupProxy <Boolean>] [-FirewallExceptionForWakeupProxy <WakeUpProxyFirewallExceptionTypes>]
 -Name <String> [-PassThru] [-PowerManagement] [-WakeOnLanPort <Int32>]
 [-WakeupProxyDirectAccessPrefix <String>] [-WakeupProxyPort <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdatesSettingsByName
```
Set-CMClientSetting [-BatchingTimeout <Int32>] [-DeploymentEvaluationSchedule <IResultObject>]
 [-Enable <Boolean>] [-EnforceMandatory <Boolean>] -Name <String> [-PassThru] [-ScanSchedule <IResultObject>]
 [-SoftwareUpdate] [-TimeUnit <BatchingTimeoutType>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetBackgroundIntelligentTransferSettingsByName
```
Set-CMClientSetting [-Bits] [-EnableBitsMaxBandwidth <Boolean>] [-EnableDownloadOffSchedule <Boolean>]
 [-MaxBandwidthBeginHr <Int32>] [-MaxBandwidthEndHr <Int32>] [-MaxTransferRateOffSchedule <Int32>]
 [-MaxTransferRateOnSchedule <Int32>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetClientPolicySettingsByName
```
Set-CMClientSetting [-ClientPolicy] [-EnableUserPolicy <Boolean>] [-EnableUserPolicyOnInternet <Boolean>]
 [-EnableUserPolicyOnTS <Boolean>] -Name <String> [-PassThru] [-PolicyPollingMins <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetComplianceSettingsByName
```
Set-CMClientSetting [-Compliance] [-EnableComplianceEvaluation <Boolean>] [-EnableUserDataAndProfile <Boolean>]
 -Name <String> [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetComputerRestartSettingsByName
```
Set-CMClientSetting [-ComputerRestart] -Name <String> [-PassThru]
 [-RebootLogoffNotificationCountdownMins <Int32>] [-RebootLogoffNotificationFinalWindowMins <Int32>]
 [-ReplaceToastNotificationWithDialog <Boolean>] [-NoRebootEnforcement <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetEndpointProtectionSettingsByName
```
Set-CMClientSetting [-DisableFirstSignatureUpdate <Boolean>] [-Enable <Boolean>] [-EndpointProtection]
 [-ForceRebootHr <Int32>] [-InstallEndpointProtectionClient <Boolean>] -Name <String> [-PassThru]
 [-RemoveThirdParty <Boolean>] [-SuppressReboot <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetHardwareInventorySettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] [-HardwareInventory] [-InventoryReportId <String>] -Name <String>
 [-PassThru] [-Schedule <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetMobileDeviceSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] [-Enrollment] [-EnrollmentProfileName <String>] -Name <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetNetworkAccessProtectionSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] [-ForceScan <Boolean>] -Name <String> [-NetworkAccessProtection]
 [-PassThru] [-Schedule <IResultObject>] [-UseUtcForEvaluationTime <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareMeteringSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] -Name <String> [-PassThru] [-Schedule <IResultObject>]
 [-SoftwareMetering] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetSoftwareInventorySettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] -Name <String> [-PassThru] [-Schedule <IResultObject>]
 [-SoftwareInventory] [-SoftwareInventoryFileDisplayName <String>]
 [-SoftwareInventoryFileInventoriedName <String>] [-SoftwareInventoryFileName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetMeteredNetworksSettingsByName
```
Set-CMClientSetting [-MeteredNetwork] [-MeteredNetworkUsage <MeteredNetworkUsageType>] -Name <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSecurityScopeByName
```
Set-CMClientSetting -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetStateMessagingSettingsByName
```
Set-CMClientSetting -Name <String> [-PassThru] [-ReportingCycleMins <Int32>] [-StateMessage]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareDeploymentSettingsByName
```
Set-CMClientSetting -Name <String> [-PassThru] [-Schedule <IResultObject>] [-SoftwareDeployment]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMClientSetting** cmdlet changes client settings for Configuration Manager devices and users. Configuration Manager provides default values for all client settings, but you can use this cmdlet to modify settings objects. Settings objects determine settings for individual clients. For more information, see [About client settings](/mem/configmgr/core/clients/deploy/about-client-settings).

> [!IMPORTANT]
> Starting in version 2010, this cmdlet is deprecated. Use one of the cmdlets specific to the client settings group, listed in the [Related links](#related-links).

To modify a client setting, specify it by name.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a client setting

This command renames the client setting object. The new name is **Client Settings TSQA**. The command also adds a description for the client setting object.

```powershell
Set-CMClientSetting -Name "Client Settings Main" -Description "Client settings for TSQA office site." -NewName "Client Settings TSQA"
```

### Example 2: Configure power management

This command allows users to opt out of power plans and disables power management for the clients with the setting named **TSQA02**.

```powershell
Set-CMClientSetting -Name "TSQA02" -AllowUserToOptOutFromPowerPlan $True -EnablePowerManagement $False
```

### Example 3: Set state messaging reporting cycle value

This command sets a state messaging reporting cycle value of 10 minutes.

```powershell
Set-CMClientSetting -Name "TSQA02" -StateMessagingReportingCycleMinutes 10
```

### Example 4: Configure user affinity

This command configures user affinity settings for a client setting named **TSQA03**:

- It disables auto approval of affinity.
- It sets the **UserAffinityLogOnThresholdMinutes** parameter to 2800 minutes and the **UserAffinityUsageThresholdDays** parameter to 20 days. If a user uses a device for 2800 minutes over a period of 20 days, Configuration Manager creates a user device affinity.

```powershell
Set-CMClientSetting -Name "TSQA03" -AutoApproveAffinity $False -UserAffinityLogOnThresholdMinutes 2800 -UserAffinityUsageThresholdDays 20
```

### Example 5: Allow user affinity

This command changes the client setting named **TSQA04** to have a client automatically configure user device affinity from usage data.

```powershell
Set-CMClientSetting -Name "TSQA04" -AllowUserAffinity $True
```

### Example 6: Set bandwidth for client

This command changes settings for the client settings object named **TSQA05**:

- It enables maximum bandwidth for BITS transfers and enables off schedule downloads.
- It also specifies values for maximum bandwidth value from and to and maximum transfer rate on schedule.

```powershell
Set-CMClientSetting -Name "TSQA05" -EnableBITSMaxBandwidth $True EnableDownloadOffSchedule $True -MaxBandwidthValidFrom 8 -MaxBandwidthValidTo 15 -MaxTransferRateOnSchedule 1500
```

### Example 7: Configure user policies on the internet

This command changes settings for the client settings object named **TSQA06**:

- Enables user policy on the internet
- Enables user policy polling
- Sets a policy polling interval

```powershell
Set-CMClientSetting -Name "TSQA06" -EnableUserPolicyOnInternet $True -EnableUserPolicyPolling $False -EnableUserPolicyOnInternet $True -PolicyPollingInterval 50
```

### Example 8: Disable compliance evaluation

This command disables compliance evaluation for the setting named **TSQA07**.

```powershell
Set-CMClientSetting -Name "TSQA07" -EnableComplianceEvaluation $False
```

### Example 9: Set computer agent settings

This command changes settings for the client settings object named **TSQA09**:

- Specifies a portal and adds that portal to the trusted site list and allows it to have elevated trust.
- Specifies a branding title, Contoso IT.
- Enables third party orchestration.
- Sets final reminder and initial reminder intervals.
- Specifies that only administrators can install software, selects Bypass as the Windows PowerShell execution policy, and suspends a BitLocker PIN requirement.

```powershell
Set-CMClientSetting -Name "TSQA09" -AddPortalToTrustedSiteList $True -AllowPortalToHaveElevatedTrust $True -BrandingTitle "Contoso IT" -EnableThirdPartyOrchestration Yes -FinalReminderMinutesInterval 52 -InitialReminderHoursInterval 6 -InstallRestriction OnlyAdministrators -PortalUrl "https://NewInstall.Contoso.com" -PowerShellExecutionPolicy Bypass -SuspendBitLocker Always
```

### Example 10: Configure restart settings

This command sets restart logoff notification countdown duration and logoff notification final window duration for a client setting object named **TSQA11**.

```powershell
Set-CMClientSetting -Name "TSQA11" -RebootLogoffNotificationCountdownDuration 12 -RebootLogoffNotificationFinalWindowMinutes 80
```

### Example 11: Configure metered network usage

This command limits metered network usage for the client setting object named **TSQA21**.

```powershell
Set-CMClientSetting -Name "TSQA21" -MeteredNetworkUsage Limit
```

## PARAMETERS

### -AccessLevel
Specifies a level of allowed remote control access.
Valid values are:

- FullControl
- NoAccess
- None
- ViewOnly

```yaml
Type: AccessLevelType
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:
Accepted values: NoAccess, ViewOnly, FullControl

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddPortalToTrustedSiteList
Don't use this parameter. The application catalog is no longer supported.

```yaml
Type: Boolean
Parameter Sets: SetComputerAgentSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowClientChange
Indicates whether users can change policy or notification settings in Software Center.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowCloudDistributionPoint
Indicates whether a device or user can access content from a cloud-based distribution point.

```yaml
Type: Boolean
Parameter Sets: SetCloudSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPermittedViewer
```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases: AllowPermittedViewersToRemoteDesktop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPortalToHaveElevatedTrust
Indicates whether to allow a portal to have elevated trust.

```yaml
Type: Boolean
Parameter Sets: SetComputerAgentSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowRemoteControlOfUnattendedComputer
Indicates whether to allow remote control of a computer with no user logged onto that computer.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowUserAffinity
Indicates whether users can define their primary devices.

```yaml
Type: Boolean
Parameter Sets: SetUserDeviceAffinitySettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowUserToOptOutFromPowerPlan
Indicates whether to allow users to exclude a device from power management settings.

```yaml
Type: Boolean
Parameter Sets: SetPowerManagementSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationCatalogWebsitePointServerName

Don't use this parameter. The application catalog is no longer supported.

```yaml
Type: String
Parameter Sets: SetComputerAgentSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AudibleSignal
Specifies what kind of sound a client computer plays while under remote control.
This setting does not apply to remote assistance.
Valid values are:

- None
- PlayNoSound
- PlaySoundAtBeginAndEnd
- PlaySoundRepeatedly

```yaml
Type: AudibleSignalType
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:
Accepted values: PlayNoSound, PlaySoundAtBeginAndEnd, PlaySoundRepeatedly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoApproveAffinity
Indicates whether the client automatically configures user device affinity from usage data.

```yaml
Type: Boolean
Parameter Sets: SetUserDeviceAffinitySettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BatchingTimeout
Specifies a timeout value, as an integer.
Specify a value of Hours or Days by using the *TimeUnit* parameter.
When an update deadline passes, Configuration Manager deploys all updates pending within this period.

```yaml
Type: Int32
Parameter Sets: SetSoftwareUpdatesSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bits
```yaml
Type: SwitchParameter
Parameter Sets: SetBackgroundIntelligentTransferSettingsByName
Aliases: BitsSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BrandingTitle
Specifies a Configuration Manager branding title.
This branding information helps users identify Configuration Manager as a trusted source.

```yaml
Type: String
Parameter Sets: SetComputerAgentSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientPolicy
```yaml
Type: SwitchParameter
Parameter Sets: SetClientPolicySettingsByName
Aliases: ClientPolicySettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudService
```yaml
Type: SwitchParameter
Parameter Sets: SetCloudSettingsByName
Aliases: CloudServicesSettings, CloudServices

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Compliance
```yaml
Type: SwitchParameter
Parameter Sets: SetComplianceSettingsByName
Aliases: ComplianceSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerAgent
```yaml
Type: SwitchParameter
Parameter Sets: SetComputerAgentSettingsByName
Aliases: ComputerAgentSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerRestart
```yaml
Type: SwitchParameter
Parameter Sets: SetComputerRestartSettingsByName
Aliases: ComputerRestartSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentEvaluationSchedule
Specifies a deployment evaluation schedule as a schedule object.
To obtain a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetSoftwareUpdatesSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for client settings.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableFirstSignatureUpdate
Indicates whether to disable the first signature update on client from a remote source.

```yaml
Type: Boolean
Parameter Sets: SetEndpointProtectionSettingsByName
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

### -DisplayNewProgramNotification
Indicates whether Configuration Manager shows the user notifications for software availability or software installations.
If this parameter has a value of $False, the user sees only restart notifications.

```yaml
Type: Boolean
Parameter Sets: SetComputerAgentSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Indicates whether to enable client settings.

```yaml
Type: Boolean
Parameter Sets: SetPowerManagementSettingsByName, SetSoftwareUpdatesSettingsByName, SetEndpointProtectionSettingsByName, SetHardwareInventorySettingsByName, SetMobileDeviceSettingsByName, SetNetworkAccessProtectionSettingsByName, SetSoftwareMeteringSettingsByName, SetSoftwareInventorySettingsByName
Aliases: EnableEndpointProtection, EnablePowerManagement, EnableHardwareInventory, EnableDeviceEnrollment, EnableNetworkAccessProtection, EnableSoftwareMetering, EnableSoftwareUpdatesOnClient, EnableSoftwareInventory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableBitsMaxBandwidth
Specifies whether to enable maximum bandwidth for Background Intelligent Transfer Service (BITS) background transfers.

```yaml
Type: Boolean
Parameter Sets: SetBackgroundIntelligentTransferSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableComplianceEvaluation
Indicates whether to enable compliance evaluation for this client.

```yaml
Type: Boolean
Parameter Sets: SetComplianceSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDownloadOffSchedule
Specifies whether allow BITS downloads outside of a throttling window.

```yaml
Type: Boolean
Parameter Sets: SetBackgroundIntelligentTransferSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableThirdPartyOrchestration
Specifies whether Software Updates and Software Distribution agents wait for third-party software to install updates and applications.

Valid values are: Yes and No.

```yaml
Type: EnableThirdPartyOrchestrationType
Parameter Sets: SetComputerAgentSettingsByName
Aliases:
Accepted values: No, Yes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUserDataAndProfile
Indicates whether to enable user data and profile settings.

```yaml
Type: Boolean
Parameter Sets: SetComplianceSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUserPolicy
```yaml
Type: Boolean
Parameter Sets: SetClientPolicySettingsByName
Aliases: EnableUserPolicyPolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUserPolicyOnInternet
Indicates whether users receive a user policy when logged on to a computer on the Internet.
In order for users to receive user policy, you must enable user polling.
You can use the *EnableUserPolicyPolling* parameter to enable user polling.
An Internet-based management point must authenticate the user.

```yaml
Type: Boolean
Parameter Sets: SetClientPolicySettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableUserPolicyOnTS
Use this parameter to enable or disable the client setting, **Enable user policy for multiple user sessions**.

```yaml
Type: Boolean
Parameter Sets: SetClientPolicySettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWakeupProxy
```yaml
Type: Boolean
Parameter Sets: SetPowerManagementSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointProtection
```yaml
Type: SwitchParameter
Parameter Sets: SetEndpointProtectionSettingsByName
Aliases: EndpointProtectionSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnforceMandatory
Indicates whether to enforce all mandatory software update deployments that have deadlines within a specified period of time.

```yaml
Type: Boolean
Parameter Sets: SetSoftwareUpdatesSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enrollment
```yaml
Type: SwitchParameter
Parameter Sets: SetMobileDeviceSettingsByName
Aliases: EnrollmentSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnrollmentProfileName
```yaml
Type: String
Parameter Sets: SetMobileDeviceSettingsByName
Aliases: DeviceEnrollmentProfileName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FinalReminderMins
```yaml
Type: Int32
Parameter Sets: SetComputerAgentSettingsByName
Aliases: FinalReminderMinutesInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallExceptionForWakeupProxy
```yaml
Type: WakeUpProxyFirewallExceptionTypes
Parameter Sets: SetPowerManagementSettingsByName
Aliases: WindowsFirewallExceptionsForWakeUpProxy
Accepted values: None, Public, Private, Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallExceptionProfile
Specifies a firewall exception profile.
Valid values are:

- Disabled
- Domain
- Private
- Public

```yaml
Type: FirewallExceptionProfileType[]
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:
Accepted values: Disabled, Public, Private, Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceRebootHr
```yaml
Type: Int32
Parameter Sets: SetEndpointProtectionSettingsByName
Aliases: ForceRebootPeriod, ForceRebootHours

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceScan
Indicates whether to enable force scan.

```yaml
Type: Boolean
Parameter Sets: SetNetworkAccessProtectionSettingsByName
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

### -GrantRemoteControlPermissionToLocalAdministrator
Indicates whether local administrators on the server initiating a remote control connection can establish remote control sessions to this client.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HardwareInventory
```yaml
Type: SwitchParameter
Parameter Sets: SetHardwareInventorySettingsByName
Aliases: HardwareInventorySettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InitialReminderHours
```yaml
Type: Int32
Parameter Sets: SetComputerAgentSettingsByName
Aliases: InitialReminderHoursInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallEndpointProtectionClient
Indicates whether to install and enable the Endpoint Protection client on this client if it is not already installed.

```yaml
Type: Boolean
Parameter Sets: SetEndpointProtectionSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallRestriction
Specifies which users can initiate an install.
Valid values are:

- AllUsers
- NoUsers
- OnlyAdministrators
- OnlyAdministratorsAndPrimaryUsers

```yaml
Type: InstallRestrictionType
Parameter Sets: SetComputerAgentSettingsByName
Aliases:
Accepted values: AllUsers, OnlyAdministrators, OnlyAdministratorsAndPrimaryUsers, NoUsers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InterimReminderHours
```yaml
Type: Int32
Parameter Sets: SetComputerAgentSettingsByName
Aliases: InterimReminderHoursInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InventoryReportId
Specifies an inventory report ID.

```yaml
Type: String
Parameter Sets: SetHardwareInventorySettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogOnThresholdMins
```yaml
Type: Int32
Parameter Sets: SetUserDeviceAffinitySettingsByName
Aliases: UserAffinityLogOnThresholdMinutes, UserAffinityLogOnThresholdMins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageRemoteDesktopSetting
Indicates whether to allow Configuration Manager to manage Remote Desktop sessions for computers.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageSolicitedRemoteAssistance
Indicates whether to allow Configuration Manager to manage solicited remote assistance sessions.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUnsolicitedRemoteAssistance
Indicates whether to allow Configuration Manager to manage unsolicited remote assistance sessions.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxBandwidthBeginHr
```yaml
Type: Int32
Parameter Sets: SetBackgroundIntelligentTransferSettingsByName
Aliases: MaxBandwidthValidFrom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxBandwidthEndHr
```yaml
Type: Int32
Parameter Sets: SetBackgroundIntelligentTransferSettingsByName
Aliases: MaxBandwidthValidTo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxTransferRateOffSchedule
Specifies an integer value for maximum transfer rate off schedule.

```yaml
Type: Int32
Parameter Sets: SetBackgroundIntelligentTransferSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxTransferRateOnSchedule
Specifies an integer value for maximum transfer rate on schedule.

```yaml
Type: Int32
Parameter Sets: SetBackgroundIntelligentTransferSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MeteredNetwork
```yaml
Type: SwitchParameter
Parameter Sets: SetMeteredNetworksSettingsByName
Aliases: MeteredNetworkSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MeteredNetworkUsage
Specifies a type of metered network usage to allow.
Valid values are:

- Allow
- Block
- Limit
- None

```yaml
Type: MeteredNetworkUsageType
Parameter Sets: SetMeteredNetworksSettingsByName
Aliases:
Accepted values: None, Allow, Limit, Block

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for a client setting.

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

### -NetworkAccessProtection
```yaml
Type: SwitchParameter
Parameter Sets: SetNetworkAccessProtectionSettingsByName
Aliases: NetworkAccessProtectionSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for a client setting.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoRebootEnforcement

Applies to version 2006 and later. Configure the client setting **Configuration Manager can force a device to restart** to prevent devices from automatically restarting when a deployment requires it. By default, Configuration Manager can still force devices to restart. For more information, see [device restart notifications](/mem/configmgr/core/clients/deploy/device-restart-notifications).

```yaml
Type: Boolean
Parameter Sets: SetComputerRestartSettingsByName
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

### -PermittedViewer
Specifies an array of names of users who can establish remote control sessions to a client computer.

```yaml
Type: String[]
Parameter Sets: SetRemoteToolsSettingsByName
Aliases: PermittedViewers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyPollingMins
```yaml
Type: Int32
Parameter Sets: SetClientPolicySettingsByName
Aliases: PolicyPollingInterval, PollingIntervalMins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PortalUrl
Specifies a link, as a URL, for a portal for a client.

```yaml
Type: String
Parameter Sets: SetComputerAgentSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PowerManagement
```yaml
Type: SwitchParameter
Parameter Sets: SetPowerManagementSettingsByName
Aliases: PowerManagementSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PowerShellExecutionPolicy
Specifies how Configuration Manager runs Windows PowerShell scripts on remote computers.
Valid values are

- AllSigned
- Bypass
- Restricted

The default value is Restricted.

When you select Restricted, the Configuration Manager client uses the current Windows PowerShell configuration on the client computer, which determines whether unsigned scripts run.

```yaml
Type: PowerShellExecutionPolicyType
Parameter Sets: SetComputerAgentSettingsByName
Aliases:
Accepted values: AllSigned, Bypass, Restricted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Specifies a priority change for a client setting.
Valid values are: Decrease and Increase.

```yaml
Type: PriorityChangeType
Parameter Sets: SetByName
Aliases:
Accepted values: Increase, Decrease

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PromptUserForPermission
Indicates whether a client computer displays a message asking for user permission before it allows a remote control session.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RebootLogoffNotificationCountdownMins
```yaml
Type: Int32
Parameter Sets: SetComputerRestartSettingsByName
Aliases: RebootLogoffNotificationCountdownDurationMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RebootLogoffNotificationFinalWindowMins
```yaml
Type: Int32
Parameter Sets: SetComputerRestartSettingsByName
Aliases: RebootLogoffNotificationFinalWindowMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteAssistanceAccessLevel
Specifies a level of access to assign to remote assistance sessions initiated in Configuration Manager.
A user at the client computer always grants permission for a remote assistance session to occur.
Valid values are:

- FullControl
- None
- RemoteViewing

```yaml
Type: RemoteAssistanceAccessLevelType
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:
Accepted values: None, RemoteViewing, FullControl

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteControl
```yaml
Type: SwitchParameter
Parameter Sets: SetRemoteToolsSettingsByName
Aliases: RemoteToolsSettings, RemoteTools

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveThirdParty
Indicates whether to remove third party.

```yaml
Type: Boolean
Parameter Sets: SetEndpointProtectionSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplaceToastNotificationWithDialog

Specify whether to replace toast notifications with a more intrusive dialog window when a deployment requires a restart. It's an optional parameter and false by default.

```yaml
Type: Boolean
Parameter Sets: SetComputerRestartSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportingCycleMins
```yaml
Type: Int32
Parameter Sets: SetStateMessagingSettingsByName
Aliases: StateMessagingReportingCycleMinutes, StateMessagingReportingCycleMins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireAuthentication
Indicates whether to use network-level authentication to establish Remote Desktop connections to a client computer.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScanSchedule
Specifies a scan schedule as a schedule object.
To obtain a schedule object, use the **New-CMSchedule** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetSoftwareUpdatesSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a **CMSchedule** object.
To create a **CMSchedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetComplianceSettingsByName, SetHardwareInventorySettingsByName, SetNetworkAccessProtectionSettingsByName, SetSoftwareMeteringSettingsByName, SetSoftwareInventorySettingsByName, SetSoftwareDeploymentSettingsByName
Aliases: InventorySchedule, NapEvaluationSchedule, EvaluationSchedule, DataCollectionSchedule, SoftwareInventorySchedule

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelectApplicationCatalogWebsitePoint

Don't use this parameter. The application catalog is no longer supported.

```yaml
Type: ApplicationCatalogWebsitePointType
Parameter Sets: SetComputerAgentSettingsByName
Aliases:
Accepted values: Fqdn, AutoDetect, NetBios

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowNotificationIconOnTaskbar
Indicates whether to display an icon on the taskbar of a client computer to indicate an active remote control session.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowSessionConnectionBar
Indicates whether to display a high-visibility session connection bar on a client computer to specify an active remote control session.

```yaml
Type: Boolean
Parameter Sets: SetRemoteToolsSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareDeployment
```yaml
Type: SwitchParameter
Parameter Sets: SetSoftwareDeploymentSettingsByName
Aliases: SoftwareDeploymentSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInventory
```yaml
Type: SwitchParameter
Parameter Sets: SetSoftwareInventorySettingsByName
Aliases: SoftwareInventorySettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInventoryFileDisplayName
Specifies the display name to use in place of an inventoried name specified by the *SoftwareInventoryFileInventoriedName* parameter.
This parameter allows you to standardize inventory information for software names that differ in different file headers.

```yaml
Type: String
Parameter Sets: SetSoftwareInventorySettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInventoryFileInventoriedName
Specifies an inventoried manufacturer or product name.
During software inventory, Configuration Manager gets inventoried names from header information on client devices.

```yaml
Type: String
Parameter Sets: SetSoftwareInventorySettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInventoryFileName
Specifies a name for the file you want to collect during inventory.
You can use the wildcard (*) to represent any string of text and the question mark (?) to represent any single character.

```yaml
Type: String
Parameter Sets: SetSoftwareInventorySettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareMetering
```yaml
Type: SwitchParameter
Parameter Sets: SetSoftwareMeteringSettingsByName
Aliases: SoftwareMeteringSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdate
```yaml
Type: SwitchParameter
Parameter Sets: SetSoftwareUpdatesSettingsByName
Aliases: SoftwareUpdatesSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StateMessage
```yaml
Type: SwitchParameter
Parameter Sets: SetStateMessagingSettingsByName
Aliases: StateMessageSettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuppressReboot
Indicates whether to bypass a required computer restart after installing the System Center 2016 Endpoint Protection client.

```yaml
Type: Boolean
Parameter Sets: SetEndpointProtectionSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuspendBitLocker
Specifies whether to bypass a required BitLocker Drive Encryption PIN entry when a computer restarts after a software installation.
This setting applies only when Configuration Manager initiates a restart.
Valid values are:

- Always.
Configuration Manager temporarily suspends the BitLocker requirement to enter a PIN.
- Never.
Configuration Manager does not suspend the BitLocker requirement to enter a PIN on the next computer startup after it has installed software that requires a restart.

If you select Never, the software installation cannot finish until the user enters the PIN to complete the standard startup process.

```yaml
Type: SuspendBitLockerType
Parameter Sets: SetComputerAgentSettingsByName
Aliases:
Accepted values: Never, Always

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeUnit
Specifies the unit for the value specified in the *BatchingTimeout* parameter.
Valid values are: Hours and Days.

```yaml
Type: BatchingTimeoutType
Parameter Sets: SetSoftwareUpdatesSettingsByName
Aliases:
Accepted values: Days, Hours

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UsageThresholdDays
```yaml
Type: Int32
Parameter Sets: SetUserDeviceAffinitySettingsByName
Aliases: UserAffinityUsageThresholdDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseNewSoftwareCenter
```yaml
Type: Boolean
Parameter Sets: SetComputerAgentSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDeviceAffinity
```yaml
Type: SwitchParameter
Parameter Sets: SetUserDeviceAffinitySettingsByName
Aliases: UserDeviceAffinitySettings

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtcForEvaluationTime
Indicates whether to use Coordinated Universal Time (UTC), also known as Greenwich Mean Time, to configure a recurring interval.
If you specify $False, Configuration Manager uses local time.

```yaml
Type: Boolean
Parameter Sets: SetNetworkAccessProtectionSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeOnLanPort
```yaml
Type: Int32
Parameter Sets: SetPowerManagementSettingsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeupProxyDirectAccessPrefix
```yaml
Type: String
Parameter Sets: SetPowerManagementSettingsByName
Aliases: IPv6PrefixesForDirectAccessOrInterveningNetworkDevices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeupProxyPort
```yaml
Type: Int32
Parameter Sets: SetPowerManagementSettingsByName
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

### None
## OUTPUTS

### System.Object
## NOTES

Starting in version 2010, this cmdlet is deprecated. Use one of the cmdlets specific to the client settings group, listed in the [Related links](#related-links).

## RELATED LINKS

[About client settings](/mem/configmgr/core/clients/deploy/about-client-settings)

[Get-CMClientSetting](Get-CMClientSetting.md)

[New-CMClientSetting](New-CMClientSetting.md)

[Remove-CMClientSetting](Remove-CMClientSetting.md)

[New-CMSchedule](New-CMSchedule.md)

[Set-CMClientSettingBackgroundIntelligentTransfer](Set-CMClientSettingBackgroundIntelligentTransfer.md)
[Set-CMClientSettingClientCache](Set-CMClientSettingClientCache.md)
[Set-CMClientSettingClientPolicy](Set-CMClientSettingClientPolicy.md)
[Set-CMClientSettingCloudService](Set-CMClientSettingCloudService.md)
[Set-CMClientSettingComplianceSetting](Set-CMClientSettingComplianceSetting.md)
[Set-CMClientSettingComputerAgent](Set-CMClientSettingComputerAgent.md)
[Set-CMClientSettingComputerRestart](Set-CMClientSettingComputerRestart.md)
[Set-CMClientSettingDeliveryOptimization](Set-CMClientSettingDeliveryOptimization.md)
[Set-CMClientSettingEndpointProtection](Set-CMClientSettingEndpointProtection.md)
[Set-CMClientSettingEnrollment](Set-CMClientSettingEnrollment.md)
[Set-CMClientSettingGeneral](Set-CMClientSettingGeneral.md)
[Set-CMClientSettingHardwareInventory](Set-CMClientSettingHardwareInventory.md)
[Set-CMClientSettingMeteredInternetConnection](Set-CMClientSettingMeteredInternetConnection.md)
[Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md)
[Set-CMClientSettingRemoteTool](Set-CMClientSettingRemoteTool.md)
[Set-CMClientSettingSoftwareCenter](Set-CMClientSettingSoftwareCenter.md)
[Set-CMClientSettingSoftwareDeployment](Set-CMClientSettingSoftwareDeployment.md)
[Set-CMClientSettingSoftwareInventory](Set-CMClientSettingSoftwareInventory.md)
[Set-CMClientSettingSoftwareMetering](Set-CMClientSettingSoftwareMetering.md)
[Set-CMClientSettingSoftwareUpdate](Set-CMClientSettingSoftwareUpdate.md)
[Set-CMClientSettingStateMessaging](Set-CMClientSettingStateMessaging.md)
[Set-CMClientSettingUserAndDeviceAffinity](Set-CMClientSettingUserAndDeviceAffinity.md)
