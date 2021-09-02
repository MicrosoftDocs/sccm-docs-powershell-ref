---
description: Modifies the properties of an access account.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMAccessAccount
---

# Set-CMAccessAccount

## SYNOPSIS
Modifies the properties of an access account.

## SYNTAX

### SearchByValue (Default)
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> [-InputObject] <IResultObject>
 [-PassThru] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByApplicationId
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -ApplicationId <String> [-PassThru]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByApplicationName
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -ApplicationName <String>
 [-PassThru] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByBootImageId
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -BootImageId <String> [-PassThru]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByBootImageName
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -BootImageName <String> [-PassThru]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByDriverPackageId
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -DriverPackageId <String>
 [-PassThru] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByDriverPackageName
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -DriverPackageName <String>
 [-PassThru] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSImageId
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -OperatingSystemImageId <String>
 [-PassThru] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSImageName
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -OperatingSystemImageName <String>
 [-PassThru] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSInstallerId
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -OperatingSystemInstallerId <String>
 [-PassThru] [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSInstallerName
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType>
 -OperatingSystemInstallerName <String> [-PassThru] [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByPackageId
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -PackageId <String> [-PassThru]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByPackageName
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> -PackageName <String> [-PassThru]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageId
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> [-PassThru]
 -SoftwareUpdateDeploymentPackageId <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageName
```
Set-CMAccessAccount -Access <AccessRight> -AccountType <AccessAccountType> [-PassThru]
 -SoftwareUpdateDeploymentPackageName <String> [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAccessAccount** cmdlet modifies the properties of an access account.
You can add users or groups to the access account and change the level of permissions to objects to which they have permissions.

An access account is a list of users or groups that can access an established service or application that is located on a distribution point.
For example, members in the Software Update Point Connection Access Account can access two services to manage software updates: Windows Server Update Services (WSUS) and WSUS Synchronization Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change access to a package by using the package name
```
PS XYZ:\> $Name = Get-CMAccessAccount -PackageName "Configuration Manager Client Package"
PS XYZ:\> Set-CMAccessAccount -PackageName $Name -Type User -UserName "CONTOSO\PFuller" -Access Read -Confirm
```

The first command gets the package name, and then stores it in the $Name variable.

The second command sets access permissions for the user to the package to Read.
You must confirm the action before the command performs it.

## PARAMETERS

### -Access
Specifies the access rights that are associated with an access account.
Valid values are: No Access, Read, Change, and Full Control.

```yaml
Type: AccessRight
Parameter Sets: (All)
Aliases:
Accepted values: NoAccess, Read, Change, FullControl

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountType
Specifies an account type.
Valid values are: Guest, User, WindowsGroup, and WindowsUser.

```yaml
Type: AccessAccountType
Parameter Sets: (All)
Aliases:
Accepted values: User, Guest, Administrator, WindowsUser, WindowsGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Specifies the name of an application.

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
Specifies the ID of a deployed software script or program.

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
Specifies the name of a deployed software script or program.

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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -SoftwareUpdateDeploymentPackageId
Specifies the ID of a deployed software update.

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
Specifies the name of a deployed software update.

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
Specifies a Windows user account name in domain\user format.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMAccessAccount](Get-CMAccessAccount.md)

[New-CMAccessAccount](New-CMAccessAccount.md)

[Remove-CMAccessAccount](Remove-CMAccessAccount.md)

[Get-CMApplication](Get-CMApplication.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](Get-CMPackage.md)

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)


