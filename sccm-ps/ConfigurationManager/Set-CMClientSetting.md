---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
ms.assetid: 0F088B51-F0AF-4A8C-AD75-8FD1665B8CDF
online version: https://go.microsoft.com/fwlink/?linkid=833719
schema: 2.0.0
---

# Set-CMClientSetting

## SYNOPSIS
Changes client settings for Configuration Manager devices and users.

## SYNTAX

### SetByName (Default)
```
Set-CMClientSetting -Name <String> [-NewName <String>] [-Description <String>] [-Priority <PriorityChangeType>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetEndpointProtectionSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] -Name <String> [-EndpointProtection]
 [-InstallEndpointProtectionClient <Boolean>] [-RemoveThirdParty <Boolean>] [-SuppressReboot <Boolean>]
 [-ForceRebootHr <Int32>] [-DisableFirstSignatureUpdate <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetPowerManagementSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] -Name <String> [-PowerManagement]
 [-AllowUserToOptOutFromPowerPlan <Boolean>] [-EnableWakeupProxy <Boolean>] [-WakeupProxyPort <Int32>]
 [-WakeOnLanPort <Int32>] [-FirewallExceptionForWakeupProxy <WakeUpProxyFirewallExceptionTypes>]
 [-WakeupProxyDirectAccessPrefix <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetHardwareInventorySettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] [-Schedule <IResultObject>] -Name <String> [-HardwareInventory]
 [-InventoryReportId <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetMobileDeviceSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] -Name <String> [-Enrollment] [-EnrollmentProfileName <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetNetworkAccessProtectionSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] [-Schedule <IResultObject>] -Name <String> [-NetworkAccessProtection]
 [-UseUtcForEvaluationTime <Boolean>] [-ForceScan <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareMeteringSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] [-Schedule <IResultObject>] -Name <String> [-SoftwareMetering]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareUpdatesSettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] -Name <String> [-SoftwareUpdate] [-ScanSchedule <IResultObject>]
 [-DeploymentEvaluationSchedule <IResultObject>] [-BatchingTimeout <Int32>] [-EnforceMandatory <Boolean>]
 [-TimeUnit <BatchingTimeoutType>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetSoftwareInventorySettingsByName
```
Set-CMClientSetting [-Enable <Boolean>] [-Schedule <IResultObject>] -Name <String> [-SoftwareInventory]
 [-SoftwareInventoryFileName <String>] [-SoftwareInventoryFileDisplayName <String>]
 [-SoftwareInventoryFileInventoriedName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSoftwareDeploymentSettingsByName
```
Set-CMClientSetting [-Schedule <IResultObject>] -Name <String> [-SoftwareDeployment] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetComplianceSettingsByName
```
Set-CMClientSetting [-Schedule <IResultObject>] -Name <String> [-Compliance]
 [-EnableComplianceEvaluation <Boolean>] [-EnableUserDataAndProfile <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCloudSettingsByName
```
Set-CMClientSetting -Name <String> [-CloudService] [-AllowCloudDistributionPoint <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSecurityScopeByName
```
Set-CMClientSetting -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetStateMessagingSettingsByName
```
Set-CMClientSetting -Name <String> [-StateMessage] [-ReportingCycleMins <Int32>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetUserDeviceAffinitySettingsByName
```
Set-CMClientSetting -Name <String> [-UserDeviceAffinity] [-LogOnThresholdMins <Int32>]
 [-UsageThresholdDays <Int32>] [-AutoApproveAffinity <Boolean>] [-AllowUserAffinity <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetBackgroundIntelligentTransferSettingsByName
```
Set-CMClientSetting -Name <String> [-Bits] [-EnableBitsMaxBandwidth <Boolean>] [-MaxBandwidthBeginHr <Int32>]
 [-MaxBandwidthEndHr <Int32>] [-MaxTransferRateOnSchedule <Int32>] [-EnableDownloadOffSchedule <Boolean>]
 [-MaxTransferRateOffSchedule <Int32>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetClientPolicySettingsByName
```
Set-CMClientSetting -Name <String> [-ClientPolicy] [-PolicyPollingMins <Int32>] [-EnableUserPolicy <Boolean>]
 [-EnableUserPolicyOnInternet <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetComputerAgentSettingsByName
```
Set-CMClientSetting -Name <String> [-ComputerAgent] [-InitialReminderHours <Int32>]
 [-InterimReminderHours <Int32>] [-FinalReminderMins <Int32>] [-PortalUrl <String>]
 [-AddPortalToTrustedSiteList <Boolean>] [-AllowPortalToHaveElevatedTrust <Boolean>]
 [-SelectApplicationCatalogWebsitePoint <ApplicationCatalogWebsitePointType>]
 [-ApplicationCatalogWebsitePointServerName <String>] [-BrandingTitle <String>]
 [-UseNewSoftwareCenter <Boolean>] [-InstallRestriction <InstallRestrictionType>]
 [-SuspendBitLocker <SuspendBitLockerType>]
 [-EnableThirdPartyOrchestration <EnableThirdPartyOrchestrationType>]
 [-PowerShellExecutionPolicy <PowerShellExecutionPolicyType>] [-DisplayNewProgramNotification <Boolean>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetComputerRestartSettingsByName
```
Set-CMClientSetting -Name <String> [-ComputerRestart] [-RebootLogoffNotificationCountdownMins <Int32>]
 [-RebootLogoffNotificationFinalWindowMins <Int32>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetMeteredNetworksSettingsByName
```
Set-CMClientSetting -Name <String> [-MeteredNetwork] [-MeteredNetworkUsage <MeteredNetworkUsageType>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetRemoteToolsSettingsByName
```
Set-CMClientSetting -Name <String> [-RemoteControl]
 [-FirewallExceptionProfile <FirewallExceptionProfileType[]>] [-AllowClientChange <Boolean>]
 [-AllowRemoteControlOfUnattendedComputer <Boolean>] [-PromptUserForPermission <Boolean>]
 [-GrantRemoteControlPermissionToLocalAdministrator <Boolean>] [-AccessLevel <AccessLevelType>]
 [-PermittedViewer <String[]>] [-ShowNotificationIconOnTaskbar <Boolean>] [-ShowSessionConnectionBar <Boolean>]
 [-AudibleSignal <AudibleSignalType>] [-ManageUnsolicitedRemoteAssistance <Boolean>]
 [-ManageSolicitedRemoteAssistance <Boolean>] [-RemoteAssistanceAccessLevel <RemoteAssistanceAccessLevelType>]
 [-ManageRemoteDesktopSetting <Boolean>] [-AllowPermittedViewer <Boolean>] [-RequireAuthentication <Boolean>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMClientSetting** cmdlet changes client settings for Microsoft System Center Configuration Manager devices and users.
System Center Configuration Manager provides default values for all client settings, but you can use this cmdlet to modify settings objects.
Settings objects determine settings for individual clients.
For more information about client settings, see [About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226) on TechNet.

Client settings for devices include the following categories:

- Client Policy
- Computer Agent
- Computer Restart
- System Center 2016 Endpoint Protection
- Hardware Inventory
- Metered Internet Connections
- Network Access Protection (NAP)
- Power Options
- Remote Tools
- Software Deployment
- Software Inventory
- Software Updates
- User and Device Affinity

Client settings for users include the following categories:

- Mobile Devices
- User and Device Affinity

To modify a client setting, specify it by name.

## EXAMPLES

### Example 1: Rename a client setting
```
PS C:\> Set-CMClientSetting -Name "Client Settings Main" -Description "Client settings for TSQA office site." -NewName "Client Settings TSQA"
```

This command renames the client setting object.
The new name is Client Settings TSQA.
The command also adds a description for the client setting object.

### Example 2: Configure power management
```
PS C:\> Set-CMClientSetting -Name "TSQA02" -AllowUserToOptOutFromPowerPlan $True -EnablePowerManagement $False
```

This command allows users to opt out of power plans and disables power management for the clients with the setting named TSQA02.

### Example 3: Set state messaging reporting cycle value
```
PS C:\> Set-CMClientSetting -Name "TSQA02" -StateMessagingReportingCycleMinutes 10
```

This command sets a state messaging reporting cycle value of 10 minutes.

### Example 4: Configure user affinity
```
PS C:\> Set-CMClientSetting -Name "TSQA03" -AutoApproveAffinity $False -UserAffinityLogOnThresholdMinutes 2800 -UserAffinityUsageThresholdDays 20
```

This command configures user affinity settings for a client setting named TSQA03.
The command disables auto approval of affinity.
The command sets the *UserAffinityLogOnThresholdMinutes* parameter to 2800 minutes and the *UserAffinityUsageThresholdDays* parameter to 20 days, so if a user uses a device for 2800 minutes over a period of 20 days, Configuration Manager creates a user device affinity.

### Example 5: Allow user affinity
```
PS C:\> Set-CMClientSetting -Name "TSQA04" -AllowUserAffinity $True
```

This command changes the client setting named TSQA04 to have a client automatically configure user device affinity from usage data.

### Example 6: Set bandwidth for client
```
PS C:\> Set-CMClientSetting -Name "TSQA05" -EnableBITSMaxBandwidth $True EnableDownloadOffSchedule $True -MaxBandwidthValidFrom 8 -MaxBandwidthValidTo 15 -MaxTransferRateOnSchedule 1500
```

This command changes settings for the client settings object named TSQA05.
The command enables maximum bandwidth for BITS transfers and enables off schedule downloads.
The command also specifies values for maximum bandwidth value from and to and maximum transfer rate on schedule.

### Example 7: Configure user policies on the Internet
```
PS C:\> Set-CMClientSetting -Name "TSQA06" -EnableUserPolicyOnInternet $True -EnableUserPolicyPolling $False -EnableUserPolicyOnInternet $True -PolicyPollingInterval 50
```

This command changes settings for the client settings object named TSQA06.
The command enables user policy on the Internet, enables user policy polling, and sets a policy polling interval.

### Example 8: Disable compliance evaluation
```
PS C:\> Set-CMClientSetting -Name "TSQA07" -EnableComplianceEvaluation $False
```

This command disables compliance evaluation for the setting named TSQA07.

### Example 9: Set computer agent settings
```
PS C:\> Set-CMClientSetting -Name "TSQA09" -AddPortalToTrustedSiteList $True -AllowPortalToHaveElevatedTrust $True -BrandingTitle "Contoso IT" -EnableThirdPartyOrchestration Yes -FinalReminderMinutesInterval 52 -InitialReminderHoursInterval 6 -InstallRestriction OnlyAdministrators -PortalUrl "http://NewInstall.Contoso.com" -PowerShellExecutionPolicy Bypass -SuspendBitLocker Always
```

This command changes settings for the client settings object named TSQA09.
The command specifies a portal and adds that portal to the trusted site list and allows it to have elevated trust.
The command specifies a branding title, Contoso IT.
The command enables third party orchestration.
The command sets final reminder and initial reminder intervals.
The command also specifies that only administrators can install software, selects Bypass as the Windows PowerShell execution policy, and suspends a BitLocker PIN requirement.

### Example 10: Configure restart settings
```
PS C:\> Set-CMClientSetting -Name "TSQA11" -RebootLogoffNotificationCountdownDuration 12 -RebootLogoffNotificationFinalWindowMinutes 80
```

This command sets restart logoff notification countdown duration and logoff notification final window duration for a client setting object named TSQA11.

### Example 11: Configure metered network usage
```
PS C:\> Set-CMClientSetting -Name "TSQA21" -MeteredNetworkUsage Limit
```

This command specifies the type of metered network usage for the client setting object named TSQA21 as Limit.

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
Indicates whether to add the default Application Catalog website to the Internet Explorer trusted sites zone.

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
Parameter Sets: SetEndpointProtectionSettingsByName, SetPowerManagementSettingsByName, SetHardwareInventorySettingsByName, SetMobileDeviceSettingsByName, SetNetworkAccessProtectionSettingsByName, SetSoftwareMeteringSettingsByName, SetSoftwareUpdatesSettingsByName, SetSoftwareInventorySettingsByName
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

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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
Parameter Sets: SetHardwareInventorySettingsByName, SetNetworkAccessProtectionSettingsByName, SetSoftwareMeteringSettingsByName, SetSoftwareInventorySettingsByName, SetSoftwareDeploymentSettingsByName, SetComplianceSettingsByName
Aliases: InventorySchedule, NapEvaluationSchedule, EvaluationSchedule, DataCollectionSchedule, SoftwareInventorySchedule

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelectApplicationCatalogWebsitePoint
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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226)

[Get-CMClientSetting](Get-CMClientSetting.md)

[New-CMClientSetting](New-CMClientSetting.md)

[Remove-CMClientSetting](Remove-CMClientSetting.md)

[New-CMSchedule](New-CMSchedule.md)
