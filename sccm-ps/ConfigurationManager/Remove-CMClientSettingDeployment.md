---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Remove-CMClientSettingDeployment

## SYNOPSIS

Remove a specific deployment of a custom client setting.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMClientSettingDeployment [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMClientSettingDeployment -CollectionId <String> -ClientSettingsId <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a specific deployment of a custom client setting. When you deploy custom settings, they override the default client settings. Custom client settings with a higher priority can also override other settings. For more information, see [Create and deploy custom client settings](/mem/configmgr/core/clients/deploy/configure-client-settings#create-and-deploy-custom-client-settings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a client setting deployment by ID

This example removes the deployment of the **Remote control** client settings to the collection with ID **XYZ0003F**.

```powershell
$clientSettingId = (Get-CMClientSetting -Name "Remote control").SettingsID

Remove-CMClientSettingDeployment -CollectionID 'XYZ0003F' -ClientSettingsID $clientSettingId
```

## PARAMETERS

### -ClientSettingsId

Specify the ID of the client settings that's deployed. This ID is the **Settings ID** in the console, and the **SettingsID** property on the **SMS_ClientSettings** WMI class.

You can use the [Get-CMClientSetting](Get-CMClientSetting.md) cmdlet to get this property. For example, `(Get-CMClientSetting -Name "Remote control").SettingsID`

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

Specify the collection ID to which the client settings are deployed. This value is the standard collection ID format, for example, `XYZ00042`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
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

### -InputObject

Specify a client settings deployment object to remove.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Deployment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[New-CMClientSettingDeployment](New-CMClientSettingDeployment.md)

[Get-CMClientSetting](Get-CMClientSetting.md)

[Create and deploy custom client settings](/mem/configmgr/core/clients/deploy/configure-client-settings#create-and-deploy-custom-client-settings)
