---
description: Saves an Endpoint Protection definition.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Save-CMEndpointProtectionDefinition
---

# Save-CMEndpointProtectionDefinition

## SYNOPSIS
Saves an Endpoint Protection definition.

## SYNTAX

### SearchByValueMandatory (Default)
```
Save-CMEndpointProtectionDefinition [-Device <IResultObject>] -DeviceCollection <IResultObject>
 [-DeviceId <String>] [-DeviceName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Save-CMEndpointProtectionDefinition [-Device <IResultObject>] -DeviceCollectionName <String>
 [-DeviceId <String>] [-DeviceName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Save-CMEndpointProtectionDefinition [-Device <IResultObject>] -DeviceCollectionId <String> [-DeviceId <String>]
 [-DeviceName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Save-CMEndpointProtectionDefinition** cmdlet saves a System Center 2016 Endpoint Protection definition in Configuration Manager.
Endpoint Protection definitions contain anti-malware policies and settings for Windows Firewall that you can apply to specific groups of computers.

For more information about Endpoint Protection, see [Endpoint Protection in Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Save an Endpoint Protection epshort definition by using a device collection nameepshortEndpoint Protection
```
PS XYZ:\> Save-CMEndpointProtectionDefinition -DeviceCollectionName "NA-Client-Devices"
```

This command saves the Endpoint Protection definition to the devices in the device collection named NA-Client-Devices.

## PARAMETERS

### -Device
Specifies a device object in Configuration Manager.
To obtain a device object, use the [Get-CMDevice](Get-CMDevice.md) cmdlet.
This object identifies the device to which you save the Endpoint Protection definition.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceCollection
Specifies a device collection object in Configuration Manager.
To obtain a device collection object, use the [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlet.
This object identifies the device collection to which you save the Endpoint Protection definition.

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

### -DeviceCollectionId
Specifies an ID for a Configuration Manager device collection to which you add the Endpoint Protection definition.

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

### -DeviceCollectionName
Specifies a name for a Configuration Manager device collection to which you add the Endpoint Protection definition.

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

### -DeviceId
Specifies the ID of a Configuration Manager device to which you add the Endpoint Protection definition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies the name of a Configuration Manager device to which you save the Endpoint Protection definition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Endpoint Protection in Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection)

[Add-CMEndpointProtectionPoint](Add-CMEndpointProtectionPoint.md)

[Get-CMEndpointProtectionPoint](Get-CMEndpointProtectionPoint.md)

[Remove-CMEndpointProtectionPoint](Remove-CMEndpointProtectionPoint.md)

[Get-CMDevice](Get-CMDevice.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)


