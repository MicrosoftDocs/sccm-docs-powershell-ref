---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833640
schema: 2.0.0
ms.assetid: 776836A3-581F-4989-8FBD-67C811B4983E
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

## EXAMPLES

### Example 1: Get a device collection variable by name
```
PS C:\>Get-CMDeviceCollectionVariable -CollectionName "DeviceCollection02" -VariableName "testTS"
```

This command gets the collection variable named testTS for the device collection named Device.

## PARAMETERS

### -Collection
Specifies a device collection object.
To obtain a collection object, use the [Get-CMCollection](./Get-CMCollection.md) cmdlet.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Planning a Task Sequence Strategy in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=260806)

[Set-CMDeviceCollectionVariable](./Set-CMDeviceCollectionVariable.md)

[New-CMDeviceCollectionVariable](./New-CMDeviceCollectionVariable.md)

[Remove-CMDeviceCollectionVariable](./Remove-CMDeviceCollectionVariable.md)

[Get-CMUserCollection](./Get-CMUserCollection.md)


