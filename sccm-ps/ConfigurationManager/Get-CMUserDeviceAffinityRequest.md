---
description: Gets a request for user device affinity in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMUserDeviceAffinityRequest
---

# Get-CMUserDeviceAffinityRequest

## SYNOPSIS
Gets a request for user device affinity in Configuration Manager.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMUserDeviceAffinityRequest -CollectionName <String> [-DeviceId <String>] [-DeviceName <String>]
 [-UserId <String>] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMUserDeviceAffinityRequest -CollectionId <String> [-DeviceId <String>] [-DeviceName <String>]
 [-UserId <String>] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserDeviceAffinityRequest** cmdlet gets a request for user device affinity.

In Configuration Manager, user device affinity defines a relationship between a user and a device.
Instead of deploying an application to a group of devices, you deploy an application to a user and Configuration Manager installs the application on all devices associated with the user.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a request for user device affinity
```
PS XYZ:\> Get-CMUserDeviceAffinityRequest -CollectionName "All Systems"
```

This command gets a request for user device affinity for the collection named All Systems.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_UserMachineRelationship
### IResultObject#SMS_UserMachineRelationship
## NOTES

## RELATED LINKS

[Approve-CMUserDeviceAffinityRequest](Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](Deny-CMUserDeviceAffinityRequest.md)


