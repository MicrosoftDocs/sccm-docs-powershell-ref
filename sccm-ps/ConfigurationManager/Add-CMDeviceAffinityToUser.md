---
description: Adds device affinity to a Configuration Manager user.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMDeviceAffinityToUser
---

# Add-CMDeviceAffinityToUser

## SYNOPSIS
Adds device affinity to a Configuration Manager user.

## SYNTAX

### AddDeviceAffinityByUserName (Default)
```
Add-CMDeviceAffinityToUser [-DeviceId <Int32[]>] [-DeviceName <String[]>] -UserName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeviceAffinityByUserId
```
Add-CMDeviceAffinityToUser [-DeviceId <Int32[]>] [-DeviceName <String[]>] -UserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDeviceAffinityToUser** cmdlet adds device affinity to a user of Configuration Manager.

Device affinity in Configuration Manager associates a user with one or more devices.
Instead of deploying applications to all the user's devices, you deploy the application to the user and Configuration Manager automatically installs the application on all devices that are associated with that user.
Device affinity removes the need for Configuration Manager to determine the names of the devices of a user before you deploy applications for that user.

For more information, see [Link users and devices with user device affinity](/sccm/apps/deploy-use/link-users-and-devices-with-user-device-affinity).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add device affinity to a user by user ID
```
PS XYZ:\>Add-CMDeviceAffinityToUser -UserName "Patti Fuller" -DeviceName "WestDivUpdates05"
```

This command adds affinity to the device named WestDivUpdates05 for the user named Patti Fuller.

## PARAMETERS

### -DeviceId
Specifies a device by using an ID.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: DeviceIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies a device by using a name.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DeviceNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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
Specifies a user by using an ID.

```yaml
Type: Int32
Parameter Sets: AddDeviceAffinityByUserId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies an array of user names to associate with the device.

```yaml
Type: String[]
Parameter Sets: AddDeviceAffinityByUserName
Aliases: UniqueUserName

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Approve-CMUserDeviceAffinityRequest](Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](Deny-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinity](Get-CMUserDeviceAffinity.md)

[Get-CMUserDeviceAffinityRequest](Get-CMUserDeviceAffinityRequest.md)

[Import-CMUserDeviceAffinity](Import-CMUserDeviceAffinity.md)

[Remove-CMDeviceAffinityFromUser](Remove-CMDeviceAffinityFromUser.md)


