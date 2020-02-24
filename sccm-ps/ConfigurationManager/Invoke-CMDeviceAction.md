---
author: aczechowski
description: Initiates a remote action on a mobile device.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Invoke-CMDeviceAction
titleSuffix: Configuration Manager
---

# Invoke-CMDeviceAction

## SYNOPSIS
Initiates a remote action on a mobile device.

## SYNTAX

### ByValue (Default)
```
Invoke-CMDeviceAction [-InputObject] <IResultObject> [-Action] <DeviceActionType> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Invoke-CMDeviceAction [-Name] <String> [-Action] <DeviceActionType> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Invoke-CMDeviceAction [-Id] <Int32> [-Action] <DeviceActionType> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMDeviceAction** cmdlet initiates a remote action, such as locking or resetting a PIN for, a mobile device.
This cmdlet only works on mobile devices.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Lock a mobile device
```
PS XYZ:\> Get-CMDevice -Name "WindowsPhone0401" | Invoke-CMDeviceAction -Action Lock
```

This command gets the device object named WindowsPhone0401 and uses the pipeline operator to pass the object to **Invoke-CMDeviceAction**, which locks the device.

### Example 2: Reset the PIN for a mobile device
```
PS XYZ:\> Invoke-CMDeviceAction -Name "WindowsPhone0402" -Action PinReset -PassThru
```

This command resets the PIN for the device named WindowsPhone0402.

## PARAMETERS

### -Action
Specifies the action you want to initiate on the device.
Valid values are:

- Lock
- PinReset
- BypassActivationLock
- RequestNewActivationLockCode
- Unknown

```yaml
Type: DeviceActionType
Parameter Sets: (All)
Aliases:
Accepted values: Lock, PinReset, BypassActivationLock, RequestNewActivationLockCode

Required: True
Position: 1
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

### -Id
Specifies an ID for a device.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a device object.
To obtain a device object, use the [Get-CMDevice](Get-CMDevice.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Device

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a device.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Returns the current working object.
By default, this cmdlet does not generate any output.

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

[Get-CMDevice](Get-CMDevice.md)


