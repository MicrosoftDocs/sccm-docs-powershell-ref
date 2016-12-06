---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834094
schema: 2.0.0
ms.assetid: 5336F6B8-3B01-4D9B-8925-9FB913735BBB
---

# Install-CMClient

## SYNOPSIS
Installs a Configuration Manager client.

## SYNTAX

### SearchByDeviceValueMandatory (Default)
```
Install-CMClient -Device <IResultObject> [-IncludeDomainController <Boolean>] [-AlwaysInstallClient <Boolean>]
 [-ForceReinstall <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Install-CMClient -Name <String> [-IncludeDomainController <Boolean>] [-AlwaysInstallClient <Boolean>]
 [-ForceReinstall <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Install-CMClient -CollectionId <String> [-IncludeDomainController <Boolean>] [-AlwaysInstallClient <Boolean>]
 [-ForceReinstall <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Install-CMClient -InputObject <IResultObject> [-IncludeDomainController <Boolean>]
 [-AlwaysInstallClient <Boolean>] [-ForceReinstall <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Install-CMClient -DeviceName <String> [-IncludeDomainController <Boolean>] [-AlwaysInstallClient <Boolean>]
 [-ForceReinstall <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Install-CMClient -DeviceId <String> [-IncludeDomainController <Boolean>] [-AlwaysInstallClient <Boolean>]
 [-ForceReinstall <Boolean>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Install-CMClient** cmdlet installs a client for Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Install a client
```
PS C:\>Install-CMClient -Name "RemoteClient05" -SiteCode "CM1" -AlwaysInstallClient $True -IncludeDomainController $True
```

This command installs the client named RemoteClient05 on the Configuration Manager site that has the site code CM1.

## PARAMETERS

### -AlwaysInstallClient
Indicates whether Configuration Manager always installs the client.

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

### -CollectionId
Specifies the ID of the collection to which the client belongs.

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Device
Specifies a Configuration Manager device object.
You can get a Configuration Manager device object by using the Get-CMDevice cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByDeviceValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceId
Specifies the ID for the device to which Configuration Manager installs the client.

```yaml
Type: String
Parameter Sets: SearchByDeviceIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies the name of the device to which Configuration Manager installs the client.

```yaml
Type: String
Parameter Sets: SearchByDeviceNameMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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

### -ForceReinstall
Indicates whether the cmdlet reinstalls the client.

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

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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

### -IncludeDomainController
Indicates whether Configuration Manager authenticates and authorizes the client by using the clients domain controller.

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

### -InputObject
Specifies a Configuration Manager client object.
You can get a Configuration Manager client object by using the Get-CMBaseline cmdlet.

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
Specifies the name of a Configuration Manager client.

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

### -SiteCode
Specifies the site code for the Configuration Manager site that hosts this site system role.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMClientSetting](./Get-CMClientSetting.md)

[New-CMClientSetting](./New-CMClientSetting.md)

[Remove-CMClientSetting](./Remove-CMClientSetting.md)

[Set-CMClientSetting](./Set-CMClientSetting.md)

[Set-CMClientStatusSetting](./Set-CMClientStatusSetting.md)

[Update-CMClientStatus](./Update-CMClientStatus.md)

[Get-CMDevice](./Get-CMDevice.md)

[Get-CMBaseline](./Get-CMBaseline.md)


