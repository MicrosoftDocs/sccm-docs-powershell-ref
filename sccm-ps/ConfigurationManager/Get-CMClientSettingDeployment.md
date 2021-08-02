---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/02/2021
online version:
schema: 2.0.0
---

# Get-CMClientSettingDeployment

## SYNOPSIS

Get a deployment of a custom client settings object.

## SYNTAX

### SearchByClientSettingName (Default)
```
Get-CMClientSettingDeployment -Name <String> [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByClientSettingId
```
Get-CMClientSettingDeployment -Id <String> [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByClientSettingValue
```
Get-CMClientSettingDeployment -InputObject <IResultObject> [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to get a deployment of a custom client settings object. You can use this object with [Remove-CMClientSettingDeployment](remove-cmclientsettingdeployment.md).

For more information on client settings, see [How to configure client settings](/mem/configmgr/core/clients/deploy/configure-client-settings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the deployment of a client setting by name

This example first gets a client settings object by name, and then passes that object to Get-CMClientSettingDeployment to show details about the deployment.

```powershell
$clientSetting =  Get-CMClientSetting -Name "Software Center customizations"
$clientSetting | Get-CMClientSettingDeployment
```

## PARAMETERS

### -Collection

Specify a collection object to which the client settings object is deployed. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify the ID of a collection to which the client settings object is deployed. For example, `XYZ00012`.

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

Specify the name of a collection to which the client settings object is deployed.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

Specify the ID of the client settings object that's deployed. The **settings ID** is an integer value, for example `47` or `16777225`.

```yaml
Type: String
Parameter Sets: SearchByClientSettingId
Aliases: ClientSettingsId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a client settings object to get its deployments. To get this object, use the [Get-CMClientSetting](Get-CMClientSetting.md) cmdlet.

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

Specify the name of the client settings object that's deployed.

```yaml
Type: String
Parameter Sets: SearchByClientSettingName
Aliases: ClientSettingsName

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

### IResultObject[]#SMS_ClientSettingsAssignment

### IResultObject#SMS_ClientSettingsAssignment

## NOTES

For more information on this return object and its properties, see [SMS_ClientSettingsAssignment server WMI class](/mem/configmgr/develop/reference/core/clients/config/sms_clientsettingsassignment-server-wmi-class).

## RELATED LINKS

[New-CMClientSettingDeployment](New-CMClientSettingDeployment.md)

[Remove-CMClientSettingDeployment](remove-cmclientsettingdeployment.md)

[Get-CMClientSetting](Get-CMClientSetting.md)

[Create and deploy custom client settings](/mem/configmgr/core/clients/deploy/configure-client-settings#create-and-deploy-custom-client-settings)
