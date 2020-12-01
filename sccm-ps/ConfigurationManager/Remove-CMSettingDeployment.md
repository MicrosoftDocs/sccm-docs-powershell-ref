---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Remove-CMSettingDeployment

## SYNOPSIS

Remove a deployment for a settings policy object.

## SYNTAX

```
Remove-CMSettingDeployment [-CMSettingsDeployment] <SettingsDeployment> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Delete a deployment for a settings policy object. For example, remove the deployment of a BitLocker management policy or a Microsoft Defender Application Control policy.

## EXAMPLES

### Example 1: Remove all deployments for a BitLocker management settings object

This example first gets a BitLocker management settings object. It then uses the pipe operator to get all deployments for that policy object, and deletes those deployments.

```powershell
Get-CMBlmSetting -Name "My BitLocker settings" | Get-CMSettingDeployment | Remove-CMSettingDeployment
```

### Example 2: Remove all deployments to a specific collection for a Microsoft Defender Application Control settings object

This example first gets a Microsoft Defender Application Control settings object. It then uses the pipe operator to get all deployments for that policy object. The **Where-Object** clause filters the list of deployments to those to the **All Desktop and Server Clients** collection, andr deletes those deployments.

```powershell
Get-CMWdacSetting -Name "My App Control settings" | Get-CMSettingDeployment | Where-Object { $_.CollectionId -eq (Get-CMCollection -Name "All Desktop and Server Clients").CollectionId } | Remove-CMSettingDeployment
```

## PARAMETERS

### -CMSettingsDeployment

Specify the settings deployment object to configure. To get the deployment object, use the [Get-CMSettingDeployment](Get-CMSettingDeployment.md) cmdlet.

```yaml
Type: SettingsDeployment
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

### -Force

Run the command without asking for confirmation.

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

### Microsoft.ConfigurationManagement.Cmdlets.Deployments.Commands.SettingsDeployment

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.Deployments.Commands.SettingsDeployment

## NOTES

## RELATED LINKS

[Get-CMSettingDeployment](Get-CMSettingDeployment.md)

[New-CMSettingDeployment](New-CMSettingDeployment.md)

[Set-CMSettingDeployment](Set-CMSettingDeployment.md)
