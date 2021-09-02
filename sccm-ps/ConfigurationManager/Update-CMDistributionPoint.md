---
description: Update content on a distribution point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2020
schema: 2.0.0
title: Update-CMDistributionPoint
---

# Update-CMDistributionPoint

## SYNOPSIS

Update content on a distribution point.

## SYNTAX

### ByValue (Default)
```
Update-CMDistributionPoint -InputObject <IResultObject> [-ReloadBootImage] [-DisableWildcardHandling]
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

Use this cmdlet to update distribution points with the latest content for clients to download.

If you manually update a distribution point, it doesn't interfere with a recurring update schedule.

For more information, see [Deploy and manage content in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/deploy-and-manage-content#update-content).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Update distribution points by package name

This command updates all distribution points that have the package named **Package01**.

```powershell
Update-CMDistributionPoint -PackageName "Package01"
```

## PARAMETERS

### -ApplicationName

Specify the name of an application, and use the **DeploymentTypeName** parameter to specify the name of the deployment type with the content to update.

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

Specify the ID of a boot image to update. For example, `"XYZ00015"`.

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

Specify the name of a boot image to update.

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

### -DeploymentTypeName

Specify the name of an application deployment type to update its content. Use the **ApplicationName** parameter to specify the application.

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

Specify the ID of a driver package to update. For example, `"XYZ00017"`.

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

Specify the name of a driver package to update.

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

### -InputObject

Specify an object type to update. To get these objects, use one of the following cmdlets:

- [Get-CMPackage](Get-CMPackage.md) for a legacy package
- [Get-CMBootImage](Get-CMBootImage.md) for a boot image
- [Get-CMDeploymentPackage](Get-CMDeploymentPackage.md) for a software update deployment package
- [Get-CMDriverPackage](Get-CMDriverPackage.md) for a driver package
- [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) for an OS image
- [Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md) for an OS upgrade package

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

Specify the UNC path of a Microsoft App-V virtual application's XML manifest file.

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

Specify the ID of an OS image to update. For example, `"XYZ00018"`.

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

Specify the name of an OS image to update.

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

Specify the ID of an OS upgrade package to update. For example, `"XYZ00019"`.

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

Specify the name of an OS upgrade package to update.

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

Specify the ID of a legacy package to update. For example, `"XYZ00020"`.

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

Specify the name of a legacy package to update.

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

When you update a boot image, add this parameter to reload it with the current Windows PE version from the Windows ADK. For more information, see [Manage boot images in Configuration Manager](/mem/configmgr/osd/get-started/manage-boot-images#update-distribution-points-with-the-boot-image).

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

Specify the ID of a software update deployment package to update. For example, `"XYZ00016"`.

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

Specify the name of a software update deployment package to update.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
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

[Invoke-CMContentValidation](Invoke-CMContentValidation.md)

[Remove-CMContentDistribution](Remove-CMContentDistribution.md)

[Start-CMContentDistribution](Start-CMContentDistribution.md)
