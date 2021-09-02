---
description: Create an OS upgrade package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: New-CMOperatingSystemInstaller
---

# New-CMOperatingSystemInstaller

## SYNOPSIS

Create an OS upgrade package.

## SYNTAX

```
New-CMOperatingSystemInstaller [-Description <String>] [-Name <String>] [-Index <Int32>] -Path <String>
 [-Version <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add an OS upgrade package to a Configuration Manager site. An OS upgrade package in Configuration Manager contains the Windows setup source files to upgrade an existing OS on a computer. For more information, see [Manage OS upgrade packages with Configuration Manager](/mem/configmgr/osd/get-started/manage-operating-system-upgrade-packages).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add an OS upgrade package

This command adds an OS upgrade package named **Windows 10 latest** and specifies the network path to the installation source files.

```powershell
New-CMOperatingSystemInstaller -Name "Windows 10 latest" -Path "\\Contoso01\CM\Win10latest"
```

## PARAMETERS

### -Description

Specify an optional description to help you identify the upgrade package. The maximum length is 127 characters.

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

### -Index

When you add this parameter, the site extracts a single index image from a multi-index image. It then places the new image in the same source folder as the original image in the upgrade package source files.

Using this option results in a smaller image file, and faster offline servicing. It also supports the process to [Optimize image servicing](/mem/configmgr/osd/get-started/manage-operating-system-images#bkmk_resetbase), for a smaller image file after applying software updates.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImageIndex

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the OS upgrade package. The maximum length is 50 characters.

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

### -Path

Specify the network path to the OS upgrade package source files. The installation source files contain setup.exe and other files and folders to install the OS.

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

### -Version

Specify an optional version of the OS image. This value is for your internal versioning, not the version of the OS. The maximum length is 32 characters.

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

### IResultObject#SMS_OperatingSystemInstallPackage
## NOTES

For more information on this return object and its properties, see [SMS_OperatingSystemInstallPackage server WMI class](/mem/configmgr/develop/reference/osd/sms_operatingsysteminstallpackage-server-wmi-class).

## RELATED LINKS

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[Remove-CMOperatingSystemInstaller](Remove-CMOperatingSystemInstaller.md)

[Set-CMOperatingSystemInstaller](Set-CMOperatingSystemInstaller.md)

[Get-CMOperatingSystemUpgradeUpdateSchedule](Get-CMOperatingSystemUpgradeUpdateSchedule.md)

[Manage OS images with Configuration Manager](/mem/configmgr/osd/get-started/manage-operating-system-images)
