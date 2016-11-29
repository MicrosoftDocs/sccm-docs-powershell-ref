---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833624
schema: 2.0.0
ms.assetid: 5DD1E791-012A-468F-A016-8800E7CCE72B
---

# New-CMDeviceVariable

## SYNOPSIS
Creates a device variable.

## SYNTAX

### NewByValueMandatory (Default)
```
New-CMDeviceVariable -InputObject <IResultObject> -VariableName <String> [-VariableValue <String>]
 [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewByIdMandatory
```
New-CMDeviceVariable -DeviceId <String> -VariableName <String> [-VariableValue <String>] [-IsMask <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewByNameMandatory
```
New-CMDeviceVariable -DeviceName <String> -VariableName <String> [-VariableValue <String>] [-IsMask <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMDeviceVariable** cmdlet creates a device variable for a device.
Task sequence processing uses device variables.

## EXAMPLES

### Example 1: Create a device variable
```
PS C:\>New-CMDeviceVariable -DeviceName "gateway-server.contoso.com" -VariableName "ServerIPAddress" -VariableValue "192.168.1.1" -IsMask 0
```

This command creates a device variable for the device gateway-server.contoso.com.
The variable is named ServerIPAddress and the value is set to 192.168.1.1.
Setting the *IsMask* parameter to 0 ensures that the variable is displayed in the Configuration Manager console.

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
Specifies a device ID.

```yaml
Type: String
Parameter Sets: NewByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies a device name.
You can specify a NetBIOS name or a fully qualified domain name (FQDN).

```yaml
Type: String
Parameter Sets: NewByNameMandatory
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

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: NewByValueMandatory
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsMask
Indicates whether the variable value is displayed in the Configuration Manager console.

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

### -VariableName
Specifies the name of the device variable.

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

### -VariableValue
Specifies the value of the variable.

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

[Get-CMDeviceVariable](./Get-CMDeviceVariable.md)

[Remove-CMDeviceVariable](./Remove-CMDeviceVariable.md)

[Set-CMDeviceVariable](./Set-CMDeviceVariable.md)

[Get-CMDevice](./Get-CMDevice.md)


