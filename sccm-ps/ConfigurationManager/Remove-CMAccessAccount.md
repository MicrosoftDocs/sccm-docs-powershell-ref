---
author: aczechowski
description: Removes users or groups from an access account.
external help file: AdminUI.PS.Rba.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Remove-CMAccessAccount
titleSuffix: Configuration Manager
---

# Remove-CMAccessAccount

## SYNOPSIS
Removes users or groups from an access account.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMAccessAccount -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByApplicationName
```
Remove-CMAccessAccount -ApplicationName <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByApplicationId
```
Remove-CMAccessAccount -ApplicationId <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByBootImageName
```
Remove-CMAccessAccount -BootImageName <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByBootImageId
```
Remove-CMAccessAccount -BootImageId <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDriverPackageName
```
Remove-CMAccessAccount -DriverPackageName <String> -AccountType <AccessAccountType> [-UserName <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDriverPackageId
```
Remove-CMAccessAccount -DriverPackageId <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSImageName
```
Remove-CMAccessAccount -OperatingSystemImageName <String> -AccountType <AccessAccountType> [-UserName <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSImageId
```
Remove-CMAccessAccount -OperatingSystemImageId <String> -AccountType <AccessAccountType> [-UserName <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSInstallerName
```
Remove-CMAccessAccount -OperatingSystemInstallerName <String> -AccountType <AccessAccountType>
 [-UserName <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSInstallerId
```
Remove-CMAccessAccount -OperatingSystemInstallerId <String> -AccountType <AccessAccountType>
 [-UserName <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByPackageName
```
Remove-CMAccessAccount -PackageName <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByPackageId
```
Remove-CMAccessAccount -PackageId <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageName
```
Remove-CMAccessAccount -SoftwareUpdateDeploymentPackageName <String> -AccountType <AccessAccountType>
 [-UserName <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageId
```
Remove-CMAccessAccount -SoftwareUpdateDeploymentPackageId <String> -AccountType <AccessAccountType>
 [-UserName <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAccessAccount** cmdlet removes users or groups from an access account.

An access account is a list of users or groups that can access an established service or application that is located on a distribution point.
For example, members in the Software Update Point Connection Access Account can access two services to manage software updates: Windows Server Update Services (WSUS) and WSUS Synchronization Manager.

## EXAMPLES

### Example 1: Remove a user from an access account for an application by using its name
```
PS XYZ:\> Remove-CMAccessAccount -ApplicationName "SharePoint 2010" -Type WindowsUser -UserName "CONTOSO\ENarvaez" -Confirm
```

This command removes a Windows user from the access account for an application that is specified by using its name.
You must confirm the action before the command performs it.

### Example 2: Remove a group from an access account for a package by using its ID
```
PS XYZ:\> $ID = Get-CMAccessAccount -PackageId "CM1100002" 
PS XYZ:\> Remove-CMAccessAccount -PackageId $ID -Type WindowsGroup -UserName "CONTOSO\Guest"
```

The first command gets the package object ID, and then stores it in the variable $ID.

The second command removes a group from the access account for the specified package.
No confirmation is required.

## PARAMETERS

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

### -Force
Forces the command to run without asking for user confirmation.

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

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

[New-CMAccessAccount](New-CMAccessAccount.md)

[Get-CMAccessAccount](Get-CMAccessAccount.md)

[Set-CMAccessAccount](Set-CMAccessAccount.md)

[Get-CMApplication](Get-CMApplication.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](Get-CMPackage.md)

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)


