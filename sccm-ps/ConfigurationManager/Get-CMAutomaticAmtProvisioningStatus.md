---
title: Get-CMAutomaticAmtProvisioningStatus
titleSuffix: Configuration Manager
description: Gets the automatic provisioning status of computers with an AMT management controller.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMAutomaticAmtProvisioningStatus

## SYNOPSIS
Gets the automatic provisioning status of computers with an AMT management controller.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMAutomaticAmtProvisioningStatus -DeviceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAutomaticAmtProvisioningStatus -DeviceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMAutomaticAmtProvisioningStatus -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAutomaticAmtProvisioningStatus** cmdlet gets the current automatic provisioning status of one or more computers with an AMT management controller.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get the automatic provisioning status of a computer
```
PS XYZ:\> Get-CMAutomaticAmtProvisioningStatus -DeviceName "CMDIV-WEST03"
```

This command gets the automatic provisioning status of a computer with an AMT management controller named CMDIV-WEST03.

## PARAMETERS

### -DeviceId
Specifies an array of device IDs.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: ResourceId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of device names.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name
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

### -InputObject
Specifies a device object.
To obtain a **CMDevice** object, use the [Get-CMDevice](Get-CMDevice.md) cmdlet.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Enable-CMAutomaticAMTProvisioning](Enable-CMAutomaticAMTProvisioning.md)

[Get-CMDevice](Get-CMDevice.md)


