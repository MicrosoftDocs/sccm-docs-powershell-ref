---
description: Gets client settings.
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
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
Get-CMClientSetting [-Setting <SettingType>] [-SettingType <Types>] [-Name <String>] [-Raw]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMClientSetting [-Setting <SettingType>] [-SettingType <Types>] -Id <String> [-Raw]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientSetting** cmdlet gets a customized collection of client settings.

For more information about client settings, see [About Client Settings in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682067(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

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
Accept wildcard characters: False
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682067(v=technet.10))

[New-CMClientSetting](New-CMClientSetting.md)

[Remove-CMClientSetting](Remove-CMClientSetting.md)

[Set-CMClientSetting](Set-CMClientSetting.md)


