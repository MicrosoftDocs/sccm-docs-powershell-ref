---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834049
schema: 2.0.0
ms.assetid: FA67EA36-5834-4957-BF85-08B2C9E61193
---

# Get-CMAccessAccount

## SYNOPSIS
Gets an access account.

## SYNTAX

### SearchByApplicationName (Default)
```
Get-CMAccessAccount -ApplicationName <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByApplicationId
```
Get-CMAccessAccount -ApplicationId <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByBootImageName
```
Get-CMAccessAccount -BootImageName <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByBootImageId
```
Get-CMAccessAccount -BootImageId <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDriverPackageName
```
Get-CMAccessAccount -DriverPackageName <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDriverPackageId
```
Get-CMAccessAccount -DriverPackageId <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByOSImageName
```
Get-CMAccessAccount -OperatingSystemImageName <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByOSImageId
```
Get-CMAccessAccount -OperatingSystemImageId <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByOSInstallerName
```
Get-CMAccessAccount -OperatingSystemInstallerName <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByOSInstallerId
```
Get-CMAccessAccount -OperatingSystemInstallerId <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByPackageName
```
Get-CMAccessAccount -PackageName <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByPackageId
```
Get-CMAccessAccount -PackageId <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageName
```
Get-CMAccessAccount -SoftwareUpdateDeploymentPackageName <String> [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageId
```
Get-CMAccessAccount -SoftwareUpdateDeploymentPackageId <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMAccessAccount [-UserName <String>] [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAccessAccount** cmdlet gets an access account.

An access account is a list of users or groups that can access an established service or application that is located on a distribution point.
For example, members in the Software Update Point Connection access account can access two services to manage software updates: Windows Server Update Services (WSUS) and WSUS Synchronization Manager.
You can get an access account to change the network access permissions for clients who use the account.

## EXAMPLES

### Example 1: Get an access account for a package by using the package ID
```
PS C:\>$ID = Get-CMPackage -PackageName "Configuration Manager Client Package" 
PS C:\> Get-CMAccessAcccount -PackageId $ID
Name:          Administrator
Type:          Administrator
Access:        FullControl
Sitecode:      CM1
PackageID:     CM100002
Name:          CONTOSO\PFuller
Type:          WindowsUser
Access:        Read
Sitecode:      CM1
PackageID:     CM100002
```

The first command gets the package that is identified by name.
The command stores the ID of the specified package in the $ID variable.

The second command gets the access account for the identified package.
The command output describes all users and groups that can access this package.

### Example 2: Get an access account for a boot image by using the boot image name
```
PS C:\>Get-CMAccessAccount -BootImageName "System Image (x64)"
Name:          CONTOSO\EDaugherty
Type:          WindowsUser
Access:        Read
Sitecode:      CM1
Boot Image:    System Image (x64)
```

The command gets the access account for a system boot image that is specified by using its name.

## PARAMETERS

### -ApplicationId
Specifies the ID of an application.

```yaml
Type: String
Parameter Sets: SearchByApplicationId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies the name of an application object.

```yaml
Type: String
Parameter Sets: SearchByApplicationName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId
Specifies the ID of a boot image object.

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
Specifies the name of a boot image object.

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

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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


```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: DriverPackage, Application, OperatingSystemImage, OperatingSystemInstaller, Package, SoftwareUpdateDeploymentPackage, BootImage

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Specifies the name of an operating system installer object.

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
Specifies the ID of a deployed software script or program object.

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
Specifies the name of a deployed software script or program object.

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

### -SoftwareUpdateDeploymentPackageId
Specifies the ID of a software update deployment object.

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
Specifies the name of a deployed software update object.

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

### -UserName


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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMAccessAccount](./New-CMAccessAccount.md)

[Set-CMAccessAccount](./Set-CMAccessAccount.md)

[Remove-CMAccessAccount](./Remove-CMAccessAccount.md)

[Get-CMApplication](./Get-CMApplication.md)

[Get-CMBootImage](./Get-CMBootImage.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](./Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](./Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](./Get-CMPackage.md)

[Get-CMSoftwareUpdate](./Get-CMSoftwareUpdate.md)

[Get-CMSoftwareUpdateDeploymentPackage](./Get-CMSoftwareUpdateDeploymentPackage.md)


