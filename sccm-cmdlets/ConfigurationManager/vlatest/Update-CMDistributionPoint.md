---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834296
schema: 2.0.0
ms.assetid: C24C7EB7-412E-49ED-AC3A-D6C8838D6A87
---

# Update-CMDistributionPoint

## SYNOPSIS
Updates content on a distribution point.

## SYNTAX

### ByValue (Default)
```
Update-CMDistributionPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateByDeploymentTypeName
```
Update-CMDistributionPoint -ApplicationName <String> -DeploymentTypeName <String> [-ManifestPath <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByBootImageId
```
Update-CMDistributionPoint -BootImageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByBootImageName
```
Update-CMDistributionPoint -BootImageName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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

## EXAMPLES

### Example 1: Update distribution points by package name
```
PS C:\>Update-CMDistributionPoint -PackageName "Package01"
```

This command updates distribution points with the package named Package01.

## PARAMETERS

### -ApplicationName
Specifies the name of an application.

```yaml
Type: String
Parameter Sets: UpdateByDeploymentTypeName
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a package object.
To obtain a package object, use the [Get-CMPackage](./Get-CMPackage.md) cmdlet.

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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
Required: True
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDistributionPoint](./Get-CMDistributionPoint.md)

[Set-CMDistributionPoint](./Set-CMDistributionPoint.md)

[Remove-CMDistributionPoint](./Remove-CMDistributionPoint.md)

[Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md)

[Get-CMBootImage](./Get-CMBootImage.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](./Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](./Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](./Get-CMPackage.md)

[Get-CMSoftwareUpdateDeploymentPackage](./Get-CMSoftwareUpdateDeploymentPackage.md)
