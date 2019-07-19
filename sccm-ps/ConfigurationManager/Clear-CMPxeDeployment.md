---
title: Clear-CMPxeDeployment
titleSuffix: Configuration Manager
description: Clears the status of the most recent PXE deployment in Configuration Manager.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Clear-CMPxeDeployment

## SYNOPSIS
Clears the status of the most recent PXE deployment in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Clear-CMPxeDeployment -DeviceCollection <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Clear-CMPxeDeployment -DeviceCollectionName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Clear-CMPxeDeployment -DeviceCollectionId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_Device
```
Clear-CMPxeDeployment -DeviceName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_Device
```
Clear-CMPxeDeployment -ResourceId <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_Device
```
Clear-CMPxeDeployment -Device <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Clear-CMPxeDeployment** cmdlet clears the status of the most recent Pre-Boot EXecution Environment (PXE) deployment in Microsoft System Center Configuration Manager.

You can redeploy a required PXE deployment for a collection of devices.
Clear the status of the last PXE deployment assigned to that System Center Configuration Manager collection.
System Center Configuration Manager redeploys the most recent required deployments.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Clear a PXE deployment for a device collection
```
PS XYZ:\>Clear-CMPxeDeployment -DeviceCollectionId "SMS00072"
```

This command clears a PXE deployment identified with a device collection ID.

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

### -Device
Specifies a device object.
To obtain a device object, use the [Get-CMDevice](Get-CMDevice.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_Device
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceCollection
Specifies a device collection object.
To obtain a device collection object, use the [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceCollectionId
Specifies an array of IDs of device collections.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: CollectionId, DeviceCollectionIds, CollectionIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceCollectionName
Specifies an array of names of device collections.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory
Aliases: CollectionName, DeviceCollectionNames, CollectionNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of names of devices.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_Device
Aliases: DeviceNames

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

### -ResourceId
Specifies an array of IDs for resources.
The cmdlet clears the status of the PXE deployment for these resources.

```yaml
Type: Int32[]
Parameter Sets: SearchByIdMandatory_Device
Aliases: ResourceIds

Required: True
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

[Get-CMDevice](Get-CMDevice.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)


