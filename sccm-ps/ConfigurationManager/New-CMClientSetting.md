---
description: Creates customized client settings.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMClientSetting
---

# New-CMClientSetting

## SYNOPSIS
Creates customized client settings.

## SYNTAX

```
New-CMClientSetting [-Description <String>] -Name <String> -Type <Types> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMClientSetting** cmdlet creates a collection of customized settings for Configuration Manager client computers.
After you create the customized settings and deploy them to client computer collections, the customized settings override the default client settings for that collection.

For more information about client settings, see [About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a customized collection of client settings
```
PS XYZ:\> New-CMClientSetting -Name "Win08ClientSettings" -Description "Windows 8 Client Computers Settings" -Type 1
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

This command creates customized device settings for the group of client computers that run Windows� 8.
After the new collection of settings is created, the command displays an unpopulated list of setting properties.
To refresh and view a populated list of properties, use **Get-CMClientSetting**.
The output for this example shows a populated list.

## PARAMETERS

### -Description
Specifies a description of the content of the new settings.

```yaml
Type: String
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

### -Name
Specifies a name for customized client settings.

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

### -Type
Specifies the type of customized settings.
Valid values are: 1 (device) or 2 (user).

```yaml
Type: Types
Parameter Sets: (All)
Aliases:
Accepted values: Default, Device, User

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

### IResultObject#SMS_ClientSettings
## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings)

[Get-CMClientSetting](Get-CMClientSetting.md)

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
