---
description: Denies a request for user device affinity in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Deny-CMUserDeviceAffinityRequest
---

# Deny-CMUserDeviceAffinityRequest

## SYNOPSIS
Denies a request for user device affinity in Configuration Manager.

## SYNTAX

### SearchByNameMandatory (Default)
```
Deny-CMUserDeviceAffinityRequest -CollectionName <String> [-DeviceId <String>] [-DeviceName <String>]
 [-UserDeviceAffinityRequest <IResultObject>] [-UserDeviceAffinityRequestId <String>] [-UserId <String>]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Deny-CMUserDeviceAffinityRequest -CollectionId <String> [-DeviceId <String>] [-DeviceName <String>]
 [-UserDeviceAffinityRequest <IResultObject>] [-UserDeviceAffinityRequestId <String>] [-UserId <String>]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Deny-CMUserDeviceAffinityRequest** cmdlet denies a request for user device affinity.

In Configuration Manager, user device affinity defines a relationship between a user and a device.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Deny a request for user device affinity
```
PS XYZ:\>Deny-CMUserDeviceAffinityRequest -CollectionName "All Systems" -UserName "Western\EvanNarvaez$"
```

This command denies a request for user device affinity for the collection named All Systems.

## PARAMETERS

### -CollectionId
Specifies a collection ID that represents the user device affinity in Configuration Manager.

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

### -CollectionName
Specifies a name of a collection that represents the user device affinity in Configuration Manager.

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
Specifies a device ID in Configuration Manager.

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

### -DeviceName
Specifies a device name in Configuration Manager.

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

### -UserDeviceAffinityRequest
Specifies a **CMUserDeviceAffinityRequest** object.
To obtain a **CMUserDeviceAffinityRequest** object, use the [Get-CMUserDeviceAffinityRequest](Get-CMUserDeviceAffinityRequest.md) cmdlet.

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

### -UserDeviceAffinityRequestId
Specifies a unique ID for a request for user device affinity.

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

### -UserId
Specifies a Configuration Manager ID for a user resource.

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

### -UserName
Specifies a user name for a resource in Configuration Manager.

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

[Approve-CMUserDeviceAffinityRequest](Approve-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinityRequest](Get-CMUserDeviceAffinityRequest.md)


