---
description: Removes device affinity from a Configuration Manager user.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMDeviceAffinityFromUser
---

# Remove-CMDeviceAffinityFromUser

## SYNOPSIS
Removes device affinity from a Configuration Manager user.

## SYNTAX

### RemoveDeviceAffinityByUserName (Default)
```
Remove-CMDeviceAffinityFromUser [-DeviceId <Int32[]>] [-DeviceName <String[]>] [-Force] -UserName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDeviceAffinityByUserId
```
Remove-CMDeviceAffinityFromUser [-DeviceId <Int32[]>] [-DeviceName <String[]>] [-Force] -UserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDeviceAffinityFromUser** cmdlet removes device affinity from a user of Configuration Manager.

Device affinity in Configuration Manager associates a user with one or more devices.
Instead of deploying applications to all the devices of a user, you deploy the application to the user and Configuration Manager automatically installs the application on all devices that are associated with that user.
Device affinity removes the need for Configuration Manager to determine the names of all the devices of a user before you deploy applications for that user.

For more information about user device affinity, see [How to Manage User Device Affinity in Configuration Manager](/mem/configmgr/apps/deploy-use/link-users-and-devices-with-user-device-affinity).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove device affinity from a user by user ID
```
PS XYZ:\> Remove-CMDeviceAffinityFromUser -UserName "Patti Fuller" -DeviceName "WestDivUpdates05"
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

### -Force

Run the command without asking for confirmation.

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
Parameter Sets: RemoveDeviceAffinityByUserId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies an array of user names.

```yaml
Type: String[]
Parameter Sets: RemoveDeviceAffinityByUserName
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

[Add-CMDeviceAffinityToUser](Add-CMDeviceAffinityToUser.md)

[Approve-CMUserDeviceAffinityRequest](Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](Deny-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinity](Get-CMUserDeviceAffinity.md)

[Get-CMUserDeviceAffinityRequest](Get-CMUserDeviceAffinityRequest.md)

[Import-CMUserDeviceAffinity](Import-CMUserDeviceAffinity.md)


