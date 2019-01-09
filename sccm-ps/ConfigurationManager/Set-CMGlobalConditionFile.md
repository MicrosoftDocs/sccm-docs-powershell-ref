---
title: Set-CMGlobalConditionFile
titleSuffix: Configuration Manager
description: Sets a File System type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Set-CMGlobalConditionFile

## SYNOPSIS

Sets a File System type global condition in Configuration Manager.

## SYNTAX

### SetFileSystemFile (Default)

```powershell
Set-CMGlobalConditionFile [-FilePath <String>] [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### SetFileSystem

```powershell
Set-CMGlobalConditionFile [-Path <String>] [-FileOrFolderName <String>] [-IncludeSubfolder <Boolean>]
 [-Is64Bit <Boolean>] -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm]
```

## DESCRIPTION

The **Set-CMGlobalConditionFile** cmdlet modifies settings for a File System type global condition in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1

```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

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
Parameter Sets: SetFileSystem
Aliases: FileName, FolderName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath

Specifies the path to the specified file or folder on client computers. You can specify system environment variables and the %USERPROFILE% environment variable in the path.

```yaml
Type: String
Parameter Sets: SetFileSystemFile
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

### -IncludeSubfolder

Indicates whether you also want to search any subfolders under the specified path.

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

### -PassThru

Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -Path

Specifies the path to the specified file or folder on client computers. You can specify system environment variables and the %USERPROFILE% environment variable in the path.

```yaml
Type: String
Parameter Sets: SetFileSystem
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## OUTPUTS

### System.Object

## RELATED LINKS

- [New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)
- [Set-CMGlobalCondition](./Set-CMGlobalCondition.md)
- [Set-CMGlobalConditionActiveDirectoryQuery](./Set-CMGlobalConditionActiveDirectoryQuery.md)
- [Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)
- [Set-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)
- [Set-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)
- [Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)
- [Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)
- [Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)
- [Set-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)
- [Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)
- [Set-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXPathQuery.md)