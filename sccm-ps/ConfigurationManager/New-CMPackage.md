---
description: Creates a Configuration Manager package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMPackage
---

# New-CMPackage

## SYNOPSIS
Creates a Configuration Manager package.

## SYNTAX

### New (Default)
```
New-CMPackage [-Description <String>] [-Language <String>] [-Manufacturer <String>] -Name <String>
 [-Path <String>] [-Version <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewPackageByDefinitionNoSourceFileWithExisted
```
New-CMPackage [-FromDefinition] -PackageDefinitionName <String> [-PackageNoSourceFile]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewPackageByDefinitionNoSourceFileWithNew
```
New-CMPackage [-FromDefinition] [-PackageNoSourceFile] -PackagePath <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewPackageByDefinitionSourceFileWithExisted
```
New-CMPackage [-FromDefinition] -PackageDefinitionName <String> -SourceFileType <SourceFileType>
 -SourceFolderPath <String> -SourceFolderPathType <SourceFolderPathType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewPackageByDefinitionSourceFileWithNew
```
New-CMPackage [-FromDefinition] -PackagePath <String> -SourceFileType <SourceFileType>
 -SourceFolderPath <String> -SourceFolderPathType <SourceFolderPathType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMPackage** cmdlet creates a Configuration Manager package.
A package is a Configuration Manager object that contains the content files and instructions for distributing programs, software updates, boot images, operating system images, and drivers to Configuration Manager clients.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a package
```
PS XYZ:\> New-CMPackage -Name "ScriptsPackage01"
```

This command creates a Configuration Manager package named ScriptsPackage01.

### Example 2: Create a package and add a description
```
PS XYZ:\> New-CMPackage -Name "ScriptsPackage02" -Description "This package deploys scripts that run on a recurring schedule."
```

This command creates a Configuration Manager package named ScriptsPackage02 and adds the specified description to the package.

## PARAMETERS

### -Description
Specifies a description for the package.
You can use a maximum of 128 characters.

```yaml
Type: String
Parameter Sets: New
Aliases:

Required: False
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

### -FromDefinition
Indicates that Configuration Manager creates the package from a package definition file.

```yaml
Type: SwitchParameter
Parameter Sets: NewPackageByDefinitionNoSourceFileWithExisted, NewPackageByDefinitionNoSourceFileWithNew, NewPackageByDefinitionSourceFileWithExisted, NewPackageByDefinitionSourceFileWithNew
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Language
Specifies the language version of the package.
You can use a maximum of 32 characters in a format that you choose to use to identify the language version.
Configuration Manager uses the *Language* parameter together with *Manufacturer*, *Name*, and *Version* to identify a package.
For example, you can have an English version and a German version of the same package.

```yaml
Type: String
Parameter Sets: New
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Manufacturer
Specifies a manufacturer name to help you identify the package.
You can use a maximum of 32 characters.

```yaml
Type: String
Parameter Sets: New
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the package.

```yaml
Type: String
Parameter Sets: New
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageDefinitionName
Specifies the name of a package definition file.

```yaml
Type: String
Parameter Sets: NewPackageByDefinitionNoSourceFileWithExisted, NewPackageByDefinitionSourceFileWithExisted
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageNoSourceFile
Indicates that the package does not require source files to be present on client devices.

```yaml
Type: SwitchParameter
Parameter Sets: NewPackageByDefinitionNoSourceFileWithExisted, NewPackageByDefinitionNoSourceFileWithNew
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackagePath
Specifies a share name or path that Configuration Manager creates for the package source files on distribution points.

```yaml
Type: String
Parameter Sets: NewPackageByDefinitionNoSourceFileWithNew, NewPackageByDefinitionSourceFileWithNew
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the location of the files to add to the package.

You can specify either a full local path or a UNC path.
Make sure that this location contains all the files and subdirectories that the program needs to complete, including any scripts.

```yaml
Type: String
Parameter Sets: New
Aliases: PackageSourcePath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFileType
Specifies the source file type.
The acceptable values for this parameter are:

- AlwaysObtainSourceFile
- CreateCompressedVersionOfSourceFile

```yaml
Type: SourceFileType
Parameter Sets: NewPackageByDefinitionSourceFileWithExisted, NewPackageByDefinitionSourceFileWithNew
Aliases:
Accepted values: AlwaysObtainSourceFile, CreateCompressedVersionOfSourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFolderPath
Specifies the location of the source files for the package.

```yaml
Type: String
Parameter Sets: NewPackageByDefinitionSourceFileWithExisted, NewPackageByDefinitionSourceFileWithNew
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFolderPathType
Specifies the source folder path type.
The acceptable values for this parameter are:

- LocalFolderOnSiteServer
- UncNetworkPath

```yaml
Type: SourceFolderPathType
Parameter Sets: NewPackageByDefinitionSourceFileWithExisted, NewPackageByDefinitionSourceFileWithNew
Aliases:
Accepted values: UncNetworkPath, LocalFolderOnSiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies a version number for the package.

```yaml
Type: String
Parameter Sets: New
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

### IResultObject#SMS_Package

## NOTES

## RELATED LINKS

[Export-CMPackage](Export-CMPackage.md)

[Get-CMPackage](Get-CMPackage.md)

[Import-CMPackage](Import-CMPackage.md)

[Remove-CMPackage](Remove-CMPackage.md)

[Set-CMPackage](Set-CMPackage.md)


