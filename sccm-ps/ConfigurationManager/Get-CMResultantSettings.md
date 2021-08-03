---
description: Gets a resultant settings.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMResultantSettings
---

# Get-CMResultantSettings

## SYNOPSIS
Gets a resultant settings.

## SYNTAX

### ByName (Default)
```
Get-CMResultantSettings -Name <String> [-Setting <SettingType>] -SettingsType <ResultantSettingsType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMResultantSettings -Id <String> [-Setting <SettingType>] -SettingsType <ResultantSettingsType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMResultantSettings -InputObject <IResultObject> [-Setting <SettingType>]
 -SettingsType <ResultantSettingsType> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

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
```yaml
Type: String
Parameter Sets: ById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Device, User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: ByName
Aliases: DeviceName, UserName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Setting
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

### -SettingsType
```yaml
Type: ResultantSettingsType
Parameter Sets: (All)
Aliases:
Accepted values: Device, User

Required: True
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
