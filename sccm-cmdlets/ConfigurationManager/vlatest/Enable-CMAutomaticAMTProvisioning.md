---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833977
schema: 2.0.0
ms.assetid: 08E05ACB-B1DE-4D06-861B-E96AA2271AD8
---

# Enable-CMAutomaticAmtProvisioning

## SYNOPSIS
Enables automatic provisioning of AMT-based computers.

## SYNTAX

### SearchByValueMandatory (Default)
```
Enable-CMAutomaticAmtProvisioning -Device <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Enable-CMAutomaticAmtProvisioning -DeviceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Enable-CMAutomaticAmtProvisioning -DeviceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-CMAutomaticAMTProvisioning** cmdlet enables automatic provisioning of Intel Active Management Technology (AMT)-based computers for Microsoft System Center Configuration Manager.
After System Center Configuration Manager identifies computers with an AMT management controller from an out of band service point, you can use this cmdlet to enable automatic provision of the computers.
An out of band service point is a site system role that provisions and configures Intel Active Management Technology (AMT)-based computers for System Center Configuration Manager.

## EXAMPLES

### Example 1: Enable automatic provisioning of an AMT-based computers
```
PS C:\>Enable-CMAutomaticAmtProvisioning -DeviceName "CMdiv-west03"
```

This command enables automatic provisioning of the device named CMdiv-west03.

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
To obtain a **CMDevice** object, use the Get-CMDevice cmdlet.

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

### -DeviceId
Specifies an array of device IDs.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of device names.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name

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

[Get-CMAutomaticAmtProvisioningStatus](./Get-CMAutomaticAmtProvisioningStatus.md)

[Get-CMDevice](./Get-CMDevice.md)


