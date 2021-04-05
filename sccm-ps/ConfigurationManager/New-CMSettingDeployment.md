---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# New-CMSettingDeployment

## SYNOPSIS

Deploy a settings policy object to a collection.

## SYNTAX

```
New-CMSettingDeployment [-CMSetting] <CMSettings> [-Schedule <IResultObject>] [-OverrideServiceWindows]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Deploy a settings policy object to a collection. For example, deploy a BitLocker management policy or a Microsoft Defender Application Control policy. To create a custom schedule, use the [New-CMSchedule](New-CMSchedule.md) cmdlet. To get a collection, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

## EXAMPLES

### Example 1: Deploy a BitLocker management object to all desktop and server clients

This example gets a BitLocker management settings object by name and stores that object in the **$setting** variable. It then gets a collection by name, and stores that object in the **$collection** variable. It uses the **New-CMSettingDeployment** cmdlet to deploy the BitLocker management settings object to that collection.

```powershell
$setting = Get-CMBlmSetting -Name "My BitLocker settings"

$collection = Get-CMCollection -Name "All Desktop and Server Clients"

New-CMSettingDeployment -CMSetting $setting -CollectionName $collection.Name
```

### Example 2: Deploy a Windows Defender Application Control setting using a custom schedule

This example also creates a custom schedule using the **New-CMSchedule** cmdlet.

```powershell
$setting = Get-CMWdacSetting -Name "My App Control settings"

$collection = Get-CMCollection -Name "All Desktop and Server Clients"

$sched = New-CMSchedule -Start ((Get-Date).AddDays(-30)).ToString() -RecurCount 7 -RecurInterval Minutes

$dep = New-CMSettingDeployment -CMSetting $setting -Collection $collection -Schedule $sched
```

## PARAMETERS

### -CMSetting

Specify a settings object to deploy.

- For BitLocker management, use the [Get-CMBlmSetting](Get-CMBlmSetting.md) or [New-CMBlmSetting](New-CMBlmSetting.md) cmdlets.
- For Microsoft Defender Application Control, use the [Get-CMWdacSetting](Get-CMWdacSetting.md) or [New-CMWdacSetting](New-CMWdacSetting.md) cmdlets.

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

### -Collection

Specify a collection object as the target for the deployment. To get a collection, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

### -CollectionId

Specify the ID of the collection as the target for the deployment.

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

### -CollectionName

Specify the name of the collection as the target for the deployment.

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

### -OverrideServiceWindows

When you add this parameter, the client can remediate the settings outside of a maintenance window.

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

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.SimplifiedSettings.CMSettings

## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.Deployments.SettingsDeployment.SettingsDeployment

## NOTES

## RELATED LINKS

[Get-CMBlmSetting](Get-CMBlmSetting.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[Get-CMWdacSetting](Get-CMWdacSetting.md)

[New-CMWdacSetting](New-CMWdacSetting.md)

[Get-CMCollection](Get-CMCollection.md)

[New-CMSchedule](New-CMSchedule.md)

[Get-CMSettingDeployment](Get-CMSettingDeployment.md)

[Remove-CMSettingDeployment](Remove-CMSettingDeployment.md)

[Set-CMSettingDeployment](Set-CMSettingDeployment.md)
