---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834127
schema: 2.0.0
ms.assetid: E309D1B1-672D-4733-B145-FBA92FD748D8
---

# Get-CMAutomaticAmtProvisioningStatus

## SYNOPSIS
Gets the automatic provisioning status of computers with an AMT management controller.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMAutomaticAmtProvisioningStatus -DeviceName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAutomaticAmtProvisioningStatus -DeviceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMAutomaticAmtProvisioningStatus -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAutomaticAmtProvisioningStatus** cmdlet gets the current automatic provisioning status of one or more computers with an AMT management controller.

## EXAMPLES

### Example 1: Get the automatic provisioning status of a computer
```
PS C:\>Get-CMAutomaticAmtProvisioningStatus -DeviceName "CMDIV-WEST03"
```

This command gets the automatic provisioning status of a computer with an AMT management controller named CMDIV-WEST03.

## PARAMETERS

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

### -InputObject
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Enable-CMAutomaticAMTProvisioning](./Enable-CMAutomaticAMTProvisioning.md)

[Get-CMDevice](./Get-CMDevice.md)


