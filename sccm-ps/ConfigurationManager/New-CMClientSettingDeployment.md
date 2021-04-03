---
description: Deploy a custom client setting.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
schema: 2.0.0
title: New-CMClientSettingDeployment
---

# New-CMClientSettingDeployment

## SYNOPSIS

Deploy a custom client setting.

## SYNTAX

### SearchByClientSettingName (Default)
```
New-CMClientSettingDeployment -Name <String> [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByClientSettingId
```
New-CMClientSettingDeployment -Id <String> [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByClientSettingValue
```
New-CMClientSettingDeployment -InputObject <IResultObject> [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to deploy a custom client setting. When you deploy custom settings, they override the default client settings. Custom client settings with a higher priority can also override other settings. For more information, see [Create and deploy custom client settings](/mem/configmgr/core/clients/deploy/configure-client-settings#create-and-deploy-custom-client-settings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Deploy a client setting object by using its ID to a named collection

```powershell
New-CMClientSettingDeployment -Id "16777225" -CollectionName "General Computer Collection"
```

## PARAMETERS

### -Collection

Specify a collection object as the target for the deployment. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify an ID for the collection to target this deployment. This value is a standard collection ID, for example, `XYZ00042`.

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

Specify a collection name to target this deployment.

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

Specify the ID of the custom client settings to deploy. This ID is the **Settings ID** in the console, and the **SettingsID** property on the **SMS_ClientSettings** WMI class.

You can use the [Get-CMClientSetting](Get-CMClientSetting.md) cmdlet to get this property. For example, `(Get-CMClientSetting -Name "Remote control").SettingsID`

```yaml
Type: String
Parameter Sets: SearchByClientSettingId
Aliases: ClientSettingId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a custom client settings object to deploy. To get this object, use the [Get-CMClientSetting](Get-CMClientSetting.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByClientSettingValue
Aliases: ClientSetting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the custom client settings to deploy.

```yaml
Type: String
Parameter Sets: SearchByClientSettingName
Aliases: ClientSettingName

Required: True
Position: Named
Default value: None
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

[Remove-CMClientSettingDeployment](Remove-CMClientSettingDeployment.md)
[Start-CMClientSettingDeployment](Start-CMClientSettingDeployment.md)

[Get-CMClientSetting](Get-CMClientSetting.md)

[Create and deploy custom client settings](/mem/configmgr/core/clients/deploy/configure-client-settings#create-and-deploy-custom-client-settings)
