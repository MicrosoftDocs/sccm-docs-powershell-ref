---
description: Gets client settings.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMClientSetting
---

# Get-CMClientSetting

## SYNOPSIS
Gets client settings.

## SYNTAX

### SearchByName (Default)
```
Get-CMClientSetting [-Name <String>] [-Raw] [-Setting <SettingType>] [-SettingType <Types>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMClientSetting -Id <String> [-Raw] [-Setting <SettingType>] [-SettingType <Types>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientSetting** cmdlet gets a customized collection of client settings.

For more information about client settings, see [About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a collection of customized client settings that is specified by its name
```
PS XYZ:\> Get-CMClientSetting -Name "Windows 8 Client Computers Settings"
AgentConfigurations: {}
AssignmentCount:     0
CreatedBy:           Contoso\DChew
DateCreated:         8/04/2012 4:40:03 PM
DateModified:        8/04/2012 4:40:03 PM
Description:         Windows 8 Client Computers Settings
Enabled:             False
FeatureType:         1
Flags:               0
LastModifiedBy:      Contoso\DChew
Name:                Win08ClientSettings
Priority:            0
SecuredScopeNames:   {Default}
Settings ID:         16777220
Type:                1
UniqueID:            {0CCA6700-AE5E-4949-8FBC-AA6719775CC3}
```

This command gets client settings that have the specified name.

## PARAMETERS

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

### -Id
Specifies an array of identifiers for one or more collections of client settings.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: SettingsId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for customized client settings.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Raw
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

### -Setting
Specifies an array of setting types for one or more collections of client settings.

Valid values are:

- BackgroundIntelligentTransfer
- ClientPolicy
- Cloud
- ComplianceSettings
- ComputerAgent
- ComputerRestart
- EndpointProtection
- HardwareInventory
- MeteredNetwork
- MobileDevice
- NetworkAccessProtection
- PowerManagement
- RemoteTools
- SoftwareDeployment
- SoftwareInventory
- SoftwareMetering
- SoftwareUpdates
- StateMessaging
- UserAndDeviceAffinity

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: BackgroundIntelligentTransfer, Cloud, ClientCache, ClientPolicy, ComplianceSettings, ComputerAgent, ComputerRestart, DeliveryOptimization, EndpointProtection, HardwareInventory, MeteredNetwork, MobileDevice, NetworkAccessProtection, PowerManagement, RemoteTools, SoftwareCenter, SoftwareDeployment, SoftwareInventory, SoftwareMetering, SoftwareUpdates, StateMessaging, UserAndDeviceAffinity, WindowsAnalytics

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SettingType
```yaml
Type: Types
Parameter Sets: (All)
Aliases: Type
Accepted values: Default, Device, User

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_ClientSettings
### IResultObject#SMS_ClientSettings
### IResultObject#SMS_ClientSettingsDefault
### Dictionary<string, object>
## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings)

[New-CMClientSetting](New-CMClientSetting.md)

[Remove-CMClientSetting](Remove-CMClientSetting.md)

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
