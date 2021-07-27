---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Set-CMSettingDeployment

## SYNOPSIS

Configure an existing settings policy deployment.

## SYNTAX

```
Set-CMSettingDeployment [-CMSettingsDeployment] <SettingsDeployment> [-Schedule <IResultObject>]
 [-OverrideServiceWindows <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Configure an existing settings policy deployment. For example, configure the deployment of a BitLocker management policy or a Microsoft Defender Application Control policy.

## EXAMPLES

### Example 1: Modify the schedule for the deployment of a BitLocker management policy

This example gets a BitLocker management policy setting object by name. It then uses the pipe operator to get a deployment for that policy object. It uses the pipe operator to modify the schedule of the deployment.

```powershell
Get-CMBlmSetting -Name "My BitLocker setting" | Get-CMSettingDeployment | Set-CMSettingDeployment -Schedule (New-CMSchedule -Start ((Get-Date).AddDays(-30)).ToString() -RecurCount 7 -RecurInterval Minutes)
```

### Example 2: Configure the deployment of a Microsoft Defender Application Control policy

This example gets an Application Control policy object by name. It then uses the pipe operator to get a deployment for that policy object. It uses the pipe operator to modify the deployment to allow the client to remediate the policy outside of a maintenance window.

```powershell
Get-CMWdacSetting -Name "My App Control setting"  | Get-CMSettingDeployment | Set-CMSettingDeployment -OverrideServiceWindows
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

### -OverrideServiceWindows

When you add this parameter, the client can remediate the settings outside of a maintenance window.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -Schedule

Specify a schedule object to apply to the deployment. To create a custom schedule, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
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

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.Deployments.SettingsDeployment.SettingsDeployment
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.Deployments.SettingsDeployment.SettingsDeployment
## NOTES

## RELATED LINKS

[Get-CMSettingDeployment](Get-CMSettingDeployment.md)

[New-CMSettingDeployment](New-CMSettingDeployment.md)

[Remove-CMSettingDeployment](Remove-CMSettingDeployment.md)
