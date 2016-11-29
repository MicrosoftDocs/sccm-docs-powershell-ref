---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834060
schema: 2.0.0
ms.assetid: 510CD0D6-ECBF-4739-92D5-550921869768
---

# Remove-CMDeviceCollectionVariable

## SYNOPSIS
Removes a device collection variable.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMDeviceCollectionVariable -Collection <IResultObject> -VariableName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMDeviceCollectionVariable -CollectionId <String> -VariableName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMDeviceCollectionVariable -CollectionName <String> -VariableName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDeviceCollectionVariable** cmdlet removes a device collection variable.

## EXAMPLES

### Example 1: Remove a device collection variable
```
PS C:\>$Collection = Get-CMCollection -Name "Device" 
PS C:\> Remove-CMDeviceCollectionVariable -Collection $Collection -VariableName "testTS" -Force
```

The first command gets the device collection object named Device and stores the object in the $Collection variable.

The second command removes the device collection variable named testTS from the device collection stored in $Collection.
Specifying the *Force* parameter indicates that the user is not prompted before the variable is removed.

### Example 2: Remove a device collection variable by using the pipeline
```
PS C:\>Get-CMCollection -Name "Device" | Remove-CMDeviceCollectionVariable -VariableName "testTS" -Force
```

This command gets the device collection object named Device and uses the pipeline operator to pass the object to **Remove-CMDeviceCollectionVariable**, which removes the device collection variable named testTS from the device collection object.
Specifying the *Force* parameter indicates that the user is not prompted before the variable is removed.

## PARAMETERS

### -Collection
Specifies a device collection object.
To obtain a collection object, use the Get-CMCollection cmdlet.

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

### -Force
Forces the command to run without asking for user confirmation.

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

[Get-CMCollection](./Get-CMCollection.md)

[Get-CMDeviceCollectionVariable](./Get-CMDeviceCollectionVariable.md)

[Set-CMDeviceCollectionVariable](./Set-CMDeviceCollectionVariable.md)

[New-CMDeviceCollectionVariable](./New-CMDeviceCollectionVariable.md)


