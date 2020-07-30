---
description: Creates a File System type global condition in Configuration Manager.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/08/2019
schema: 2.0.0
title: New-CMGlobalConditionFile
---

# New-CMGlobalConditionFile

## SYNOPSIS

Creates a File System type global condition in Configuration Manager.

## SYNTAX

### NewFileSystem (Default)
```
New-CMGlobalConditionFile [-IsFolder] -Path <String> -FileOrFolderName <String> [-IncludeSubfolder <Boolean>]
 [-Is64Bit <Boolean>] -Name <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### NewFileSystemFile
```
New-CMGlobalConditionFile -FilePath <String> [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMGlobalConditionFile** cmdlet creates a File System type global condition in Microsoft System Center Configuration Manager.

A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
$GlobalFloder = New-CMGlobalConditionFile -Path c:\ -FileOrFolderName test -IsFolder $true -Name Folder
```

This command creates a File System type folder global condition in Configuration Manager.

### Example 1

```powershell
$GlobalFile = New-CMGlobalConditionFile -FilePath c:\test  -Name file
```

This command creates a File System type file global condition in Configuration Manager.

## PARAMETERS

### -Description

Specifies a description.

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

### -FileOrFolderName

Specifies the name of the file or folder object that will be searched for. You can specify system environment variables and the %USERPROFILE% environment variable in the file or folder name. You can also use the * and ? wildcards in the file name.

```yaml
Type: String
Parameter Sets: NewFileSystem
Aliases: FileName, FolderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath

Specifies the path to the specified file on client computers. You can specify system environment variables and the %USERPROFILE% environment variable in the path.

```yaml
Type: String
Parameter Sets: NewFileSystemFile
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

### -IncludeSubfolder

Enable this option if you also want to search any sub-folders under the specified path.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: IncludeSubfolders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Is64Bit

Indicates whether the 64-bit system file location (%windir%\system32) should be searched in addition to the 32-bit system file location (%windir%\syswow64) on Configuration Manager clients that run a 64-bit version of Windows.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsFolder

Indicate whether it is a folder.

```yaml
Type: SwitchParameter
Parameter Sets: NewFileSystem
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies a name.

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

### -Path

Specifies the path to the specified  folder on client computers. You can specify system environment variables and the %USERPROFILE% environment variable in the path.

```yaml
Type: String
Parameter Sets: NewFileSystem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)

[New-CMGlobalCondition](./New-CMGlobalCondition.md)

[New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)

[New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)

[New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)

[New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)

[New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)

[New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)

[New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)

[New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)

[New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)

[New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)
