---
description: Get a device driver.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Get-CMDriver
---

# Get-CMDriver

## SYNOPSIS

Get a device driver.

## SYNTAX

### SearchByName (Default)
```
Get-CMDriver [-Fast] [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDriverPackageIdMandatory
```
Get-CMDriver [-Fast] -DriverPackageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDriverPackageNameMandatory
```
Get-CMDriver [-Fast] -DriverPackageName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDriver [-Fast] -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDriverPackage
```
Get-CMDriver [-Fast] -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByCategory
```
Get-CMDriver [-Fast] [-AdministrativeCategory <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a device driver. Configuration Manager provides a driver catalog that you can use to manage the Windows device drivers in your environment. For more information, see [Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a device driver by name

This command gets the driver named **Surface Serial Hub Driver**.

```powershell
Get-CMDriver -Name "Surface Serial Hub Driver"
```

### Example 2: Get specific information about drivers from a specific manufacturer

This command gets all drivers whose name starts with **Surface** and only display three attributes.

```powershell
Get-CMDriver -Fast -Name "Surface*" | Select-Object LocalizedDisplayName,DriverVersion,DriverDate
```

### Example 3: Get all drivers for a specific category

This command gets all drivers in the **Surface** driver category.

```powershell
$category = Get-CMCategory -Name "Surface"

Get-CMDriver -Fast -AdministrativeCategory $category
```

## PARAMETERS

### -AdministrativeCategory

Specify an array of driver category objects. You can assign a driver to a category for filtering purposes. For example, "Surface" or "Boot image".

To get this object, use the [Get-CMCategory](Get-CMCategory.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: SearchByCategory
Aliases: AdministrativeCategories

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

### -DriverPackageId

Specify the ID of a driver package to get all drivers in it. This value is a standard package ID format, for example, `XYZ00204`.

```yaml
Type: String
Parameter Sets: SearchByDriverPackageIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageName

Specify the name of a driver package to get all drivers in it.

```yaml
Type: String
Parameter Sets: SearchByDriverPackageNameMandatory
Aliases: PackageName

Required: True
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

Specify the ID of a specific device driver. This value is the same as the **CI_ID** attribute, for example `66383`.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, DriverId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a driver package object to get all drivers in it. To get this object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByDriverPackage
Aliases: DriverPackage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a specific device driver to get.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName, DriverName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_Driver
### IResultObject#SMS_Driver
## NOTES

For more information on this return object and its properties, see [SMS_Driver server WMI class](/mem/configmgr/develop/reference/osd/sms_driver-server-wmi-class).

## RELATED LINKS

[Disable-CMDriver](Disable-CMDriver.md)

[Enable-CMDriver](Enable-CMDriver.md)

[Import-CMDriver](Import-CMDriver.md)

[Remove-CMDriver](Remove-CMDriver.md)

[Set-CMDriver](Set-CMDriver.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers)
