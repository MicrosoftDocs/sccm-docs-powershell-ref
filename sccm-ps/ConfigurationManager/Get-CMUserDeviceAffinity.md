---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: 465E33E8-26CF-4981-A815-0ADD2BFA15F9
online version: https://go.microsoft.com/fwlink/?linkid=834001
schema: 2.0.0
---

# Get-CMUserDeviceAffinity

## SYNOPSIS
Gets a user's device affinities.

## SYNTAX

### SearchByUserNameMandatory (Default)
```
Get-CMUserDeviceAffinity -UserName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Get-CMUserDeviceAffinity -DeviceName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Get-CMUserDeviceAffinity -DeviceId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUserIdMandatory
```
Get-CMUserDeviceAffinity -UserId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserDeviceAffinity** cmdlet gets one or more user device affinities.
User device affinity in Microsoft System Center Configuration Manager is a method of associating a user with one or more specified devices.

## EXAMPLES

### Example 1: Get a user device affinity by using a user name
```
PS C:\> Get-CMUserDeviceAffinity -UserName "CENTRAL\001D$"
```

This command gets the user device affinity for the user named CENTRAL\001D$.

### Example 2: Get a user device affinity by using a user ID
```
PS C:\> Get-CMUserDeviceAffinity -UserID "2063597981"
```

This command gets the user device affinity for the user that has the ID named 2063597981.

### Example 3: Get a user device affinity by using a device name
```
PS C:\> Get-CMUserDeviceAffinity -DeviceName "CMCEN-DIST02"
```

This command gets the user device affinity for the device named CMCEN-DIST02.

### Example 4: Get a user device affinity by using a device ID
```
PS C:\> Get-CMUserDeviceAffinity -DeviceID "2097152000"
```

This command gets the user device affinity for the device that has the ID 2097152000.

## PARAMETERS

### -DeviceId
Specifies an array of device IDs.

```yaml
Type: String[]
Parameter Sets: SearchByDeviceIdMandatory
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
Type: String[]
Parameter Sets: SearchByDeviceNameMandatory
Aliases: ResourceName

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

### -UserId
Specifies an array of IDs of the primary users of the devices.

```yaml
Type: String[]
Parameter Sets: SearchByUserIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies an array of names of the primary users of the devices.

```yaml
Type: String[]
Parameter Sets: SearchByUserNameMandatory
Aliases: UniqueUserName

Required: True
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

[Approve-CMUserDeviceAffinityRequest](Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](Deny-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinityRequest](Get-CMUserDeviceAffinityRequest.md)

[Import-CMUserDeviceAffinity](Import-CMUserDeviceAffinity.md)


