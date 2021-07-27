---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/30/2021
schema: 2.0.0
title: New-CMDriverPackage
---

# New-CMDriverPackage

## SYNOPSIS

Create a driver package.

## SYNTAX

```
New-CMDriverPackage [-Description <String>] [-DriverManufacturer <String>] [-DriverModel <String>]
 -Name <String> -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a driver package. Group similar device drivers in packages to help streamline OS deployments. For example, create a driver package for each computer manufacturer on your network. For more information, see [Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a new driver package

This command creates a new driver package named Pckg01.

```powershell
New-CMDriverPackage -Name "Pckg01" -Path "\\Contoso01\Users\pattifuller\Desktop\pckg"
```

### Example 2: Create a driver package with manufacturer and model

This command creates a driver package and specifies the manufacturer and model properties.

```powershell
New-CMDriverPackage -Name "Surface Book 2 Drivers" -Description "Some descriptive text" -DriverManufacturer "Microsoft" -DriverModel "Surface 2"
```

## PARAMETERS

### -Description

Specify an optional description of a driver package. The maximum length is 127 characters.

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

### -DriverManufacturer

Use this parameter to set the manufacturer of the device. The maximum length is 100 characters.

Use it with the **DriverModel** parameter. You can use them for managing the driver catalog, and with task sequence pre-caching. For more information, see [Configure pre-cache content for task sequences](/mem/configmgr/osd/deploy-use/configure-precache-content).

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

### -DriverModel

Use this parameter to set the model of the device. The maximum length is 100 characters.

Use it with the **DriverManufacturer** parameter. You can use them for managing the driver catalog, and with task sequence pre-caching. For more information, see [Configure pre-cache content for task sequences](/mem/configmgr/osd/deploy-use/configure-precache-content).

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

### -Name

Specify a name for a driver package. The maximum length is 50 characters.

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

### -Path

Specify a file path to the network location to source the driver files.

When you create a driver package, the source location of the package must point to an empty network share that's not used by another driver package. The SMS Provider must have **Full control** permissions to that location.

When you add device drivers to a driver package, Configuration Manager copies it to this path. You can add to a driver package only device drivers that you've imported and that are enabled in the driver catalog.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath

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

### IResultObject#SMS_DriverPackage
## NOTES

For more information on this return object and its properties, see [SMS_DriverPackage server WMI class](/mem/configmgr/develop/reference/osd/sms_driverpackage-server-wmi-class).

## RELATED LINKS

[Export-CMDriverPackage](Export-CMDriverPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Import-CMDriverPackage](Import-CMDriverPackage.md)

[Remove-CMDriverPackage](Remove-CMDriverPackage.md)

[Set-CMDriverPackage](Set-CMDriverPackage.md)

[Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers)
