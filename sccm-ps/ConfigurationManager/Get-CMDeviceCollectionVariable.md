---
description: Gets a device collection variable.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDeviceCollectionVariable
---

# Get-CMDeviceCollectionVariable

## SYNOPSIS
Gets a device collection variable.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMDeviceCollectionVariable -CollectionName <String> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMDeviceCollectionVariable -Collection <IResultObject> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDeviceCollectionVariable -CollectionId <String> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceCollectionVariable** cmdlet gets the task sequence variables for a device collection.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a device collection variable by name
```
PS XYZ:\> Get-CMDeviceCollectionVariable -CollectionName "DeviceCollection02" -VariableName "testTS"
```

This command gets the collection variable named testTS for the device collection named Device.

## PARAMETERS

### -Collection
Specifies a device collection object.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of a device collection.

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
Specifies the name of a device collection.

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

### -VariableName
Specifies the name of a collection variable.

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

### IResultObject[]#SMS_CollectionVariable

### IResultObject#SMS_CollectionVariable

## NOTES

## RELATED LINKS

[Planning a Task Sequence Strategy in Configuration Manager](/mem/configmgr/osd/plan-design/planning-considerations-for-automating-tasks)

[Set-CMDeviceCollectionVariable](Set-CMDeviceCollectionVariable.md)

[New-CMDeviceCollectionVariable](New-CMDeviceCollectionVariable.md)

[Remove-CMDeviceCollectionVariable](Remove-CMDeviceCollectionVariable.md)

[Get-CMUserCollection](Get-CMUserCollection.md)


