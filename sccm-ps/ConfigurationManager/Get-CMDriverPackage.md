---
description: Get a driver package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Get-CMDriverPackage
---

# Get-CMDriverPackage

## SYNOPSIS

Get a driver package.

## SYNTAX

### SearchByName (Default)
```
Get-CMDriverPackage [-Fast] [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDriverPackage [-Fast] -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a driver package. Group similar device drivers in packages to help streamline OS deployments. For example, create a driver package for each computer manufacturer on your network. For more information, see [Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a driver package by ID

This command gets a driver package with ID **XYZ00042**.

```powershell
Get-CMDriverPackage -Id "XYZ00042" -Fast
```

## PARAMETERS

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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

### -Id

Specify an array of IDs for a driver package. This value is a standard package ID format, for example, `XYZ00204`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of a driver package.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_DriverPackage
### IResultObject#SMS_DriverPackage
## NOTES

For more information on this return object and its properties, see [SMS_DriverPackage server WMI class](/mem/configmgr/develop/reference/osd/sms_driverpackage-server-wmi-class).

## RELATED LINKS

[Export-CMDriverPackage](Export-CMDriverPackage.md)

[Import-CMDriverPackage](Import-CMDriverPackage.md)

[New-CMDriverPackage](New-CMDriverPackage.md)

[Remove-CMDriverPackage](Remove-CMDriverPackage.md)

[Set-CMDriverPackage](Set-CMDriverPackage.md)

[Get-CMDriver](Get-CMDriver.md)

[Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers)
