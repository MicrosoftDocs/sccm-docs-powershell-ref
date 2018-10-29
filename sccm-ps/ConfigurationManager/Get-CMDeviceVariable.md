---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: 783C11B5-AF37-4B77-A78D-C43C7E1330DE
online version: https://go.microsoft.com/fwlink/?linkid=833644
schema: 2.0.0
---

# Get-CMDeviceVariable

## SYNOPSIS
Gets device variables of a Configuration Manager device.

## SYNTAX

### SearchByValueMandatory (Default)
```
Get-CMDeviceVariable -InputObject <IResultObject> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDeviceVariable -ResourceId <String> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameMandatory
```
Get-CMDeviceVariable -DeviceName <String> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceVariable** cmdlet gets device variables of a Microsoft System Center Configuration Manager device.

Individual devices have device variables. Task sequence processing uses device variables.

## EXAMPLES

### Example 1: Get a variable value by using its name
```
PS C:\> Get-CMDeviceVariable -DeviceName "Computer073" -VariableName "HostDrive"
```

This command gets the value of the variable named HostDrive for the specified computer.

## PARAMETERS

### -DeviceName
Specifies a device name.
You can specify a NetBIOS name or a fully qualified domain name (FQDN).

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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceId
Specifies a Systems Management Server (SMS) ID.

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

### -VariableName
Specifies the name of the device variable.

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

[New-CMDeviceVariable](New-CMDeviceVariable.md)

[Remove-CMDeviceVariable](Remove-CMDeviceVariable.md)

[Set-CMDeviceVariable](Set-CMDeviceVariable.md)

[Get-CMDevice](Get-CMDevice.md)


