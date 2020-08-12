---
description: Get a Configuration Manager legacy package.
external help file: AdminUI.PS.AppModel.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/06/2020
schema: 2.0.0
title: Get-CMPackage
---

# Get-CMPackage

## SYNOPSIS

Get a Configuration Manager legacy package.

## SYNTAX

### SearchByName (Default)
```
Get-CMPackage [-Name <String>] [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMPackage -Id <String> [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMPackage** cmdlet gets a Configuration Manager legacy package. You find these packages in the Configuration Manager console, **Software Library** workspace, **Application Management > Packages** node.

Other objects are considered "packages" in certain contexts, but you need to use other cmdlets to get them. For more information, see the [Related links](#related-links).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all packages

This command gets all Configuration Manager packages and stores them in the variable **$packages**.

```powershell
$packages = Get-CMPackage
```

### Example 2: Get a package by using an ID

This command gets the program that has the ID **CM100002**.

```powershell
Get-CMPackage -Id "CM100002"
```

### Example 3: Get a package by using a name

This command gets the program named **Configuration Manager Client Package**.

```powershell
Get-CMPackage -Name "Configuration Manager Client Package"
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

Does a fast query.

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

Specifies the package ID to get. For example, `"CM100002"`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies the name of a package to get. For example `"Configuration Manager Client Package"`.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_Package

### IResultObject#SMS_Package

For more information on this return object and its properties, see [SMS_Package server WMI class](https://docs.microsoft.com/mem/configmgr/develop/reference/core/servers/configure/sms_package-server-wmi-class).

## NOTES

## RELATED LINKS

[Export-CMPackage](Export-CMPackage.md)

[Import-CMPackage](Import-CMPackage.md)

[New-CMPackage](New-CMPackage.md)

[Remove-CMPackage](Remove-CMPackage.md)

[Set-CMPackage](Set-CMPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[Get-CMApplication](Get-CMApplication.md)
