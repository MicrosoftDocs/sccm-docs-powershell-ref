---
author: aczechowski
description: Updates content on a distribution point.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Update-CMDistributionPoint
titleSuffix: Configuration Manager
---

# Update-CMDistributionPoint

## SYNOPSIS
Updates content on a distribution point.

## SYNTAX

### ByValue (Default)
```
Update-CMDistributionPoint [-ReloadBootImage] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateByDeploymentTypeName
```
Update-CMDistributionPoint -ApplicationName <String> -DeploymentTypeName <String> [-ManifestPath <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByBootImageId
```
Update-CMDistributionPoint -BootImageId <String> [-ReloadBootImage] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByBootImageName
```
Update-CMDistributionPoint -BootImageName <String> [-ReloadBootImage] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDriverPackageId
```
Update-CMDistributionPoint -DriverPackageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDriverPackageName
```
Update-CMDistributionPoint -DriverPackageName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSImageId
```
Update-CMDistributionPoint -OperatingSystemImageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSImageName
```
Update-CMDistributionPoint -OperatingSystemImageName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSInstallerId
```
Update-CMDistributionPoint -OperatingSystemInstallerId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSInstallerName
```
Update-CMDistributionPoint -OperatingSystemInstallerName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByPackageId
```
Update-CMDistributionPoint -PackageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByPackageName
```
Update-CMDistributionPoint -PackageName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageId
```
Update-CMDistributionPoint -SoftwareUpdateDeploymentPackageId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageName
```
Update-CMDistributionPoint -SoftwareUpdateDeploymentPackageName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Update-CMDistributionPoint** cmdlet updates distribution points with the latest content for clients to download.
You can update the distribution points for application content, software packages, software updates, operating system images, and boot images.
Manually updating the distribution points does not interfere with the recurring update schedule.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Update distribution points by package name
```
PS XYZ:\>Update-CMDistributionPoint -PackageName "Package01"
```

This command updates distribution points with the package named Package01.

## PARAMETERS

### -ApplicationName
Specifies the name of an application.

```yaml
Type: String
Parameter Sets: UpdateByDeploymentTypeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId
Specifies the ID of a boot image.

```yaml
Type: String
Parameter Sets: SearchByBootImageId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageName
Specifies the name of a boot image.

```yaml
Type: String
Parameter Sets: SearchByBootImageName
Aliases:

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

### -DeploymentTypeName
Specifies the name of a deployment type.

```yaml
Type: String
Parameter Sets: UpdateByDeploymentTypeName
Aliases:

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

### -DriverPackageId
Specifies the ID of a driver package.

```yaml
Type: String
Parameter Sets: SearchByDriverPackageId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageName
Specifies the name of a driver package.

```yaml
Type: String
Parameter Sets: SearchByDriverPackageName
Aliases:

Required: True
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

### -InputObject
Specifies a package object.
To obtain a package object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: BootImage, DriverPackage, OperatingSystemImage, OperatingSystemInstaller, Package, SoftwareUpdateDeploymentPackage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ManifestPath
Specifies the UNC path of the virtual application's XML manifest file.
Specify the manifest path if you specify Microsoft Application Virtualization for the *DeploymentTypeName* parameter.

```yaml
Type: String
Parameter Sets: UpdateByDeploymentTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageId
Specifies the ID of an operating system image.

```yaml
Type: String
Parameter Sets: SearchByOSImageId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageName
Specifies the name of an operating system image.

```yaml
Type: String
Parameter Sets: SearchByOSImageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstallerId
Specifies the ID of an operating system installer.

```yaml
Type: String
Parameter Sets: SearchByOSInstallerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstallerName
Specifies the name of an operating system installer.

```yaml
Type: String
Parameter Sets: SearchByOSInstallerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageId
Specifies the ID of a package.

```yaml
Type: String
Parameter Sets: SearchByPackageId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName
Specifies the name of a package.

```yaml
Type: String
Parameter Sets: SearchByPackageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReloadBootImage
```yaml
Type: SwitchParameter
Parameter Sets: ByValue, SearchByBootImageId, SearchByBootImageName
Aliases: Reload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateDeploymentPackageId
Specifies the ID of a software update deployment package.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateDeploymentPackageId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateDeploymentPackageName
Specifies the name of a software update deployment package.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateDeploymentPackageName
Aliases:

Required: True
Position: Named
Default value: None
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

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Set-CMDistributionPoint](Set-CMDistributionPoint.md)

[Remove-CMDistributionPoint](Remove-CMDistributionPoint.md)

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](Get-CMPackage.md)

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)
