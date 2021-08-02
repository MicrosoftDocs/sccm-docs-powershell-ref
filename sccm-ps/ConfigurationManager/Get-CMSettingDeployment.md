---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Get-CMSettingDeployment

## SYNOPSIS

Get all of the deployments for a settings policy object.

## SYNTAX

```
Get-CMSettingDeployment [-CMSetting] <CMSettings> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Get all of the deployments for a settings policy object. For example, a BitLocker management policy or a Microsoft Defender Application Control policy. Use the [New-CMSettingDeployment](New-CMSettingDeployment.md) to deploy a policy object.

## EXAMPLES

### Example 1: Get all deployments for a BitLocker management setting

This example gets an existing BitLocker management setting object and then uses the pipe operator to get all deployments for that policy object.

```powershell
Get-CMBlmSetting -Name "My BitLocker setting" | Get-CMSettingDeployment
```

### Example 2: Get all deployments for a Microsoft Defender Application Control setting

This example gets an existing Microsoft Defender Application Control setting object, and then uses the pipe operator to get all deployments for that policy object.

```powershell
Get-CMWdacSetting -Name "My App Control setting" | Get-CMSettingDeployment
```

## PARAMETERS

### -CMSetting

Specify a settings object to get its deployments.

- For BitLocker management, use the [Get-CMBlmSetting](Get-CMBlmSetting.md) cmdlet.
- For Microsoft Defender Application Control, use the [Get-CMWdacSetting](Get-CMWdacSetting.md) cmdlet.

```yaml
Type: CMSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.SimplifiedSettings.CMSettings
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.Deployments.SettingsDeployment.SettingsDeployment
## NOTES

## RELATED LINKS

[New-CMSettingDeployment](New-CMSettingDeployment.md)

[Remove-CMSettingDeployment](Remove-CMSettingDeployment.md)

[Set-CMSettingDeployment](Set-CMSettingDeployment.md)
