---
author: aczechowski
description: Approves a device.
external help file: AdminUI.PS.Collections.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Approve-CMDevice
titleSuffix: Configuration Manager
---

# Approve-CMDevice

## SYNOPSIS
Approves a device.

## SYNTAX

### SearchByValueMandatory (Default)
```
Approve-CMDevice -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Approve-CMDevice -DeviceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Approve-CMDevice -DeviceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Approve-CMDevice** cmdlet approves one or more Microsoft System Center Configuration Manager device clients to join a site.
You cannot approve a Configuration Manager client until you have installed the device and assigned it to a site.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Approve a device
```
PS XYZ:\>Approve-CMDevice -DeviceName "TestVlan-site2"
```

This command approves the device named TestVlan-site2.

### Example 2: Get a device and approve it
```
PS XYZ:\> Get-CMDevice -Name "TestVlan-site2" | Approve-CMDevice
```

This command gets the device object named TestVlan-site2 and uses the pipeline operator to pass the object to **Approve-CMDevice**, which approves the device object.

## PARAMETERS

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

### -DeviceId
Specifies the ID of a device.

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
Specifies the name of a device.

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
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
To obtain a device object, use the [Get-CMDevice](Get-CMDevice.md) cmdlet.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Block-CMDevice](Block-CMDevice.md)

[Get-CMDevice](Get-CMDevice.md)

[Remove-CMDevice](Remove-CMDevice.md)

[Unblock-CMDevice](Unblock-CMDevice.md)


