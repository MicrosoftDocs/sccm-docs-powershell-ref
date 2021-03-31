---
description: Publishes files to a distribution point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Publish-CMPrestageContent
---

# Publish-CMPrestageContent

## SYNOPSIS
Publishes files to a distribution point.

## SYNTAX

### SearchByValueMandatory_DeploymentPackage (Default)
```
Publish-CMPrestageContent -DeploymentPackage <IResultObject> [-Description <String>]
 -DistributionPointName <String> -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_Application
```
Publish-CMPrestageContent -Application <IResultObject> [-Description <String>] [-DisableDependencyExport]
 -DistributionPointName <String> -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_Application
```
Publish-CMPrestageContent -ApplicationId <String[]> [-Description <String>] [-DisableDependencyExport]
 -DistributionPointName <String> -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_Application
```
Publish-CMPrestageContent -ApplicationName <String[]> [-Description <String>] [-DisableDependencyExport]
 -DistributionPointName <String> -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_BootImage
```
Publish-CMPrestageContent -BootImage <IResultObject> [-Description <String>] -DistributionPointName <String>
 -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory_BootImage
```
Publish-CMPrestageContent -BootImageId <String[]> [-Description <String>] -DistributionPointName <String>
 -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory_BootImage
```
Publish-CMPrestageContent -BootImageName <String[]> [-Description <String>] -DistributionPointName <String>
 -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory_DeploymentPackage
```
Publish-CMPrestageContent -DeploymentPackageId <String[]> [-Description <String>]
 -DistributionPointName <String> -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_DeploymentPackage
```
Publish-CMPrestageContent -DeploymentPackageName <String[]> [-Description <String>]
 -DistributionPointName <String> -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_DriverPackage
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -DriverPackageId <String[]>
 -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory_DriverPackage
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -DriverPackageName <String[]>
 -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory_DriverPackage
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String>
 -DriverPackage <IResultObject> -FileName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_OperatingSystemImage
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -OperatingSystemImageId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory_OperatingSystemImage
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -OperatingSystemImageName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory_OperatingSystemImage
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -OperatingSystemImage <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory_OperatingSystemInstaller
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -OperatingSystemInstallerId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_OperatingSystemInstaller
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -OperatingSystemInstallerName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_OperatingSystemInstaller
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -OperatingSystemInstaller <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_Package
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -PackageId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory_Package
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -PackageName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory_Package
```
Publish-CMPrestageContent [-Description <String>] -DistributionPointName <String> -FileName <String>
 -Package <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Publish-CMPrestageContent** cmdlet publishes files for applications, images, packages, or operating system installers to a distribution point without using the Configuration Manager distribution process.

Specify the distribution site, the file name, and the item to publish.

You can specify any of the following to publish to a distribution point:

- Application
- BootImage
- DeploymentPackage
- DriverPackage
- OperatingSystemImage
- OperatingSystemInstaller
- Package

You can specify the item to be published by name or ID, or use another cmdlet to get the desired item.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Publish a package
```
PS XYZ:\>Publish-CMPrestageContent -PackageId "CM200001" -DistributionPointName "FileDist02.Western.Contoso.com" -FileName "C:\Users\admin\Documents\Package.pkgx"
```

This command publishes the package that has the ID CM200001 to the specified distribution point as the specified .pkgx file.

### Example 2: Publish a boot image
```
PS XYZ:\>Publish-CMPrestageContent -BootImageId "CM200005" -DistributionPointName "FileDist02.Western.Contoso.com" -FileName "C:\Users\admin\Documents\BootImage.pkgx"
```

This command publishes the boot image that has the ID CM200005 to the specified distribution point as the specified .pkgx file.

### Example 3: Publish a driver package
```
PS XYZ:\>Publish-CMPrestageContent -DriverPackageId "CM20000F" -DistributionPointName "FileDist02.Western.Contoso.com" -FileName "C:\Users\admin\Documents\DriverPackage.pkgx"
```

This command publishes the driver package that has the ID CM20000F to the specified distribution point as the specified .pkgx file.

### Example 4: Publish an operating system image
```
PS XYZ:\>Publish-CMPrestageContent -OperatingSystemImageId "CM200006" -DistributionPointName "FileDist02.Western.Contoso.com" -FileName "C:\Users\admin\Documents\OSImage.pkgx"
```

This command publishes the operating system image that has the ID CM200006 to the specified distribution point as the specified .pkgx file.

### Example 5: Publish an operating system installer
```
PS XYZ:\>Publish-CMPrestageContent -OperatingSystemInstallerId "CM200017" -DistributionPointName "FileDist02.Western.Contoso.com" -FileName "C:\Users\admin\Documents\OSInstaller.pkgx"
```

This command publishes the operating system installer that has the ID CM200017 to the specified distribution point as the specified .pkgx file.

## PARAMETERS

### -Application
Specifies an application object.
To obtain an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_Application
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
Specifies an array of IDs of applications.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_Application
Aliases: ApplicationIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies an array of names of applications.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_Application
Aliases: ApplicationNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImage
Specifies a boot image object.
To obtain a boot image object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_BootImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId
Specifies an array of IDs of boot images.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_BootImage
Aliases: BootImageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageName
Specifies an array of names of boot images.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_BootImage
Aliases: BootImageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentPackage
Specifies a deployment package object.
To obtain a deployment package object, use the [Get-CMDeploymentPackage](Get-CMDeploymentPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_DeploymentPackage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentPackageId
Specifies an array of IDs of deployment packages.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_DeploymentPackage
Aliases: DeploymentPackageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentPackageName
Specifies an array of names of deployment packages.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_DeploymentPackage
Aliases: DeploymentPackageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the content.

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

### -DisableDependencyExport
```yaml
Type: SwitchParameter
Parameter Sets: SearchByValueMandatory_Application, SearchByIdMandatory_Application, SearchByNameMandatory_Application
Aliases: DisableExportAllDependencies

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

### -DistributionPointName
Specifies a distribution point for the content.

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

### -DriverPackage
Specifies a driver package object.
To obtain a driver package object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_DriverPackage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageId
Specifies an array of IDs of driver packages.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_DriverPackage
Aliases: DriverPackageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageName
Specifies an array of names of driver packages.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_DriverPackage
Aliases: DriverPackageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileName
Specifies a file name for a .pkgx file.

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

### -OperatingSystemImage
Specifies an operating system image object.
To obtain an operating system image object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_OperatingSystemImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageId
Specifies an array of IDs of operating system images.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_OperatingSystemImage
Aliases: OperatingSystemImageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageName
Specifies an array of names of operating system images.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_OperatingSystemImage
Aliases: OperatingSystemImageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstaller
Specifies an operating system installer object.
To obtain an operating system installer object, use the [Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_OperatingSystemInstaller
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstallerId
Specifies an array of IDs of operating system installers.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_OperatingSystemInstaller
Aliases: OperatingSystemInstallerIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstallerName
Specifies an array of names of operating system installers.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_OperatingSystemInstaller
Aliases: OperatingSystemInstallerNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package
Specifies a package object.
To obtain a package object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_Package
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageId
Specifies an array of IDs of packages.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_Package
Aliases: PackageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName
Specifies an array of names of packages.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_Package
Aliases: PackageNames

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDeploymentPackage](Get-CMDeploymentPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](Get-CMPackage.md)


