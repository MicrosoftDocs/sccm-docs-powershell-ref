---
description: Creates a device variable for a Configuration Manager device.
external help file: AdminUI.PS.Collections.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMDeviceVariable
---

# New-CMDeviceVariable

## SYNOPSIS
Creates a device variable for a Configuration Manager device.

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
The **New-CMDeviceVariable** cmdlet creates a device variable for a Configuration Manager device.

Individual devices have device variables. Task sequence processing uses device variables.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a device variable
```
PS XYZ:\> New-CMDeviceVariable -DeviceName "gateway-server.contoso.com" -VariableName "ServerIPAddress" -VariableValue "192.168.1.1" -IsMask 0
```

This command creates a device variable for the device gateway-server.contoso.com.
The variable is named ServerIPAddress and the value is set to 192.168.1.1.
Setting the *IsMask* parameter to 0 ensures that the variable is displayed in the Configuration Manager console.

## PARAMETERS

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
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_MachineSettings

## NOTES

## RELATED LINKS

[Get-CMDeviceVariable](Get-CMDeviceVariable.md)

[Remove-CMDeviceVariable](Remove-CMDeviceVariable.md)

[Set-CMDeviceVariable](Set-CMDeviceVariable.md)

[Get-CMDevice](Get-CMDevice.md)


