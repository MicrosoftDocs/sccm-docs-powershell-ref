---
author: aczechowski
description: Gets the state of a device action.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMDeviceActionState
titleSuffix: Configuration Manager
---

# Get-CMDeviceActionState

## SYNOPSIS
Gets the state of a device action.

## SYNTAX

### ByName (Default)
```
Get-CMDeviceActionState [[-Action] <DeviceActionType>] [[-Name] <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMDeviceActionState [[-Action] <DeviceActionType>] [-Id] <Int32> [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMDeviceActionState [[-Action] <DeviceActionType>] [-InputObject] <IResultObject> [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceActionState** cmdlet gets the state of an action initiated on a mobile device by using the [Invoke-CMDeviceAction](Invoke-CMDeviceAction.md) cmdlet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get the state of a device action using the pipeline
```
PS XYZ:\> Get-CMDevice -Name "WindowsPhone0402" | Get-CMDeviceActionState -Action PinReset
```

This command gets the device object named WindowsPhone0402 and uses the pipeline operator to pass the object to **Get-CMDeviceActionState**, which gets the state of the PIN reset action on the device.

### Example 2: Get the state of a lock action
```
PS XYZ:\> Get-CMDeviceActionState -Name "WindowsPhone0401" -Action Lock
```

This command gets the state of the lock action on the device named WindowsPhone0401.

## PARAMETERS

### -Action
Specifies the action for which you want status.
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

Required: False
Position: 1
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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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
Specifies the ID of a device.

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

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject#SMS_DeviceAction

## NOTES

## RELATED LINKS

[Get-CMDevice](Get-CMDevice.md)

[Invoke-CMDeviceAction](Invoke-CMDeviceAction.md)
