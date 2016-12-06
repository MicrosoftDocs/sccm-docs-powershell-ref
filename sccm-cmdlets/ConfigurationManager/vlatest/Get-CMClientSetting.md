---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834191
schema: 2.0.0
ms.assetid: 8316BA4A-1758-4255-A911-D5749FC64971
---

# Get-CMClientSetting

## SYNOPSIS
Gets client settings.

## SYNTAX

### SearchByName (Default)
```
Get-CMClientSetting [-Setting <SettingType>] [-SettingType <Types>] [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMClientSetting [-Setting <SettingType>] [-SettingType <Types>] -Id <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientSetting** cmdlet gets a customized collection of client settings.

For more information about client settings, see [About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226) on TechNet.

## EXAMPLES

### Example 1: Get a collection of customized client settings that is specified by its name
```
PS C:\>Get-CMClientSetting -Name "Windows 8 Client Computers Settings"
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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
Accepted values: BackgroundIntelligentTransfer, Cloud, ClientPolicy, ComplianceSettings, ComputerAgent, ComputerRestart, EndpointProtection, HardwareInventory, MeteredNetwork, MobileDevice, NetworkAccessProtection, PowerManagement, RemoteTools, SoftwareDeployment, SoftwareInventory, SoftwareMetering, SoftwareUpdates, StateMessaging, UserAndDeviceAffinity
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226)

[New-CMClientSetting](./New-CMClientSetting.md)

[Remove-CMClientSetting](./Remove-CMClientSetting.md)

[Set-CMClientSetting](./Set-CMClientSetting.md)


