---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833799
schema: 2.0.0
ms.assetid: 5FACECF3-56B3-4835-8E13-A786F65BE89D
---

# Set-CMDeviceCollectionVariable

## SYNOPSIS
Sets a device collection variable.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMDeviceCollectionVariable -InputObject <IResultObject> -VariableName <String> [-NewVariableName <String>]
 [-NewVariableValue <String>] [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByIdMandatory
```
Set-CMDeviceCollectionVariable -CollectionId <String> -VariableName <String> [-NewVariableName <String>]
 [-NewVariableValue <String>] [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMDeviceCollectionVariable -CollectionName <String> -VariableName <String> [-NewVariableName <String>]
 [-NewVariableValue <String>] [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDeviceCollectionVariable** cmdlet changes the settings of a device collection variable.

## EXAMPLES

### Example 1: Change a variable name
```
PS C:\>$Collection = Get-CMCollection -Name "Device"
PS C:\> Set-CMDeviceCollectionVariable -Collection $Collection -VariableName "testTS" -NewVariableName "NewVariable"
```

The first command gets the device collection object named Device and stores the object in the $Collection variable.

The second command changes the name of the collection variable testTS for the device collection stored in $Collection to NewVariable.

### Example 2: Change a variable name by using the pipeline
```
PS C:\>Get-CMCollection -Name "Device" | Set-CMDeviceCollectionVariable -VariableName "testTS" -NewVariableName "NewVariable"
```

This command gets the device collection object named Device and uses the pipeline operator to pass the object to **Set-CMDeviceCollectionVariable**, which changes the name of the collection variable testTS for the device collection object to NewVariable.

## PARAMETERS

### -CollectionId
Specifies the ID of a device collection.

```yaml
Type: String
Parameter Sets: SetByIdMandatory
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
Parameter Sets: SetByNameMandatory
Aliases: 
Required: True
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
Specifies a device collection object.
To obtain a collection object, use the [Get-CMCollection](./Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases: Collection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsMask
Indicates whether the collection variable value displays in the Configuration Manager console.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewVariableName
Specifies a new name for the collection variable.

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

### -NewVariableValue
Specifies a new value for the collection variable.

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

### -VariableName
Specifies the name of a collection variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
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

[Planning a Task Sequence Strategy in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=260806)

[Get-CMDeviceCollectionVariable](./Get-CMDeviceCollectionVariable.md)

[Get-CMCollection](./Get-CMCollection.md)

[New-CMDeviceCollectionVariable](./New-CMDeviceCollectionVariable.md)

[Remove-CMDeviceCollectionVariable](./Remove-CMDeviceCollectionVariable.md)

[Get-CMDeviceCollection](./Get-CMDeviceCollection.md)


