---
description: Removes client settings.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMClientSetting
---

# Remove-CMClientSetting

## SYNOPSIS
Removes client settings.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMClientSetting [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMClientSetting [-Force] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMClientSetting [-Force] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMClientSetting** cmdlet removes a customized collection of client settings.
For more information, see [About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove a collection of client settings that is specified by its ID
```
PS XYZ:\> Remove-CMClientSetting -Id "16777255"
```

This command removes a collection of client settings that is specified by the ID 16777255.
You must confirm the action before it is performed.

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

### -Force
Forces the command to run without asking for user confirmation.

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

### -InputObject
Specifies an input object for this cmdlet.
You can get an input object by using Get-CMClientSetting.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for customized client settings.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](/mem/configmgr/core/clients/deploy/about-client-settings)

[Get-CMClientSetting](Get-CMClientSetting.md)

[New-CMClientSetting](New-CMClientSetting.md)

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
