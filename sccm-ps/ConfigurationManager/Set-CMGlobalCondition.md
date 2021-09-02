---
description: Modifies settings for a Configuration Manager global condition.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/07/2019
schema: 2.0.0
title: Set-CMGlobalCondition
---

# Set-CMGlobalCondition

## SYNOPSIS

Modifies settings for a Configuration Manager global condition.

## SYNTAX

### SetGeneral (Default)
```
Set-CMGlobalCondition [-Description <String>] -Name <String> [-NewName <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetAssembly
```
Set-CMGlobalCondition [-AssemblyName <String>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetWqlQuery
```
Set-CMGlobalCondition [-Class <String>] -Name <String> [-Namespace <String>] [-PassThru] [-Property <String>]
 [-WhereClause <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetSqlQueryDefaultInstance
```
Set-CMGlobalCondition [-Column <String>] [-Database <String>] [-FilePath <String>] -Name <String> [-PassThru]
 [-UseDefaultInstance] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetSqlQueryAllInstances
```
Set-CMGlobalCondition [-Column <String>] [-Database <String>] [-FilePath <String>] -Name <String> [-PassThru]
 [-UseAllInstances] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetSqlQuerySpecificInstance
```
Set-CMGlobalCondition [-Column <String>] [-Database <String>] [-FilePath <String>] [-InstanceName <String>]
 -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetADQuery
```
Set-CMGlobalCondition [-DistinguishedName <String>] [-LdapFilter <String>] [-LdapPrefix <String>]
 -Name <String> [-PassThru] [-Property <String>] [-SearchScope <SearchScope>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetFileSystem
```
Set-CMGlobalCondition [-FileOrFolderName <String>] [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 -Name <String> [-PassThru] [-Path <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetFileSystemFile
```
Set-CMGlobalCondition [-FilePath <String>] [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] -Name <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetScript
```
Set-CMGlobalCondition [-FilePath <String>] -Name <String> [-PassThru] [-ScriptLanguage <ScriptingLanguage>]
 [-Use32BitHost <Boolean>] [-UseLoggedOnUserCredential <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetXPathQuery
```
Set-CMGlobalCondition [-FilePath <String>] [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] -Name <String>
 [-PassThru] [-XmlFilePath <String>] [-XmlNamespace <String[]>] [-XPathQuery <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetRegistryKey
```
Set-CMGlobalCondition [-Is64Bit <Boolean>] [-KeyName <String>] -Name <String> [-PassThru]
 [-RegistryHive <RegistryRootKey>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRegistryValue
```
Set-CMGlobalCondition [-Is64Bit <Boolean>] [-KeyName <String>] -Name <String> [-PassThru]
 [-RegistryHive <RegistryRootKey>] [-ValueName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetIisMetabase
```
Set-CMGlobalCondition [-MetabasePath <String>] -Name <String> [-PassThru] [-PropertyId <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetOmaUri
```
Set-CMGlobalCondition -Name <String> -OmaUri <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMGlobalCondition** cmdlet modifies settings for a global condition.
You can add or remove a security scope for a global condition.
You can specify a global condition by name or ID, or use the **Get-CMGlobalCondition** cmdlet to obtain a global condition object.

Configuration Manager uses global conditions to represent business or technical conditions.
Global conditions specify how to provide and deploy applications to client devices.

Each global condition must have at least one security scope.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a security scope

```powershell
PS XYZ:\> Set-CMGlobalCondition -Name "CPU speed" -SecurityScopeAction AddMembership -SecurityScopeName "Scope22"
```

This command adds the security scope named Scope22 to the global condition named CPU speed.

### Example 2: Remove a security scope by using a variable

```powershell
PS XYZ:\> $CMGC = Get-CMGlobalCondition -Name "CPU speed"
PS XYZ:\> Set-CMGlobalCondition -InputObject $CMGC -SecurityScopeAction RemoveMembership -SecurityScopeName "Scope22"
```

The first command uses the **Get-CMGlobalCondition** cmdlet to get the global condition named CPU speed and store it in the $CMGC variable.

The second command removes the security scope named Scope22 from the global condition stored in the $CMGC variable.

## PARAMETERS

### -AssemblyName

Specifies the name of an assembly for which to search.
An assembly name must be registered in the global assembly cache.

```yaml
Type: String
Parameter Sets: SetAssembly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Class

Specifies a Windows Management Instrumentation (WMI) class used to build a WMI Query Language (WQL) query.
The query assesses compliance on client computers.

```yaml
Type: String
Parameter Sets: SetWqlQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Column

Specifies the column name used to assess the compliance of the global condition.

```yaml
Type: String
Parameter Sets: SetSqlQueryDefaultInstance, SetSqlQueryAllInstances, SetSqlQuerySpecificInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database

Specifies the name of a database.
The SQL query runs on this database.

```yaml
Type: String
Parameter Sets: SetSqlQueryDefaultInstance, SetSqlQueryAllInstances, SetSqlQuerySpecificInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specifies a description for the global condition.

```yaml
Type: String
Parameter Sets: SetGeneral
Aliases:

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

### -DistinguishedName

Specifies the distinguished name of the Active Directory Domain Services (AD DS) object to assess for compliance on client computers.

```yaml
Type: String
Parameter Sets: SetADQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileOrFolderName

Specifies the name of a file or folder. Specify the *IsFolder* parameter to search for a folder.

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

### -FilePath

Specifies a file path for the file that the condition assesses for compliance.

```yaml
Type: String
Parameter Sets: SetSqlQueryDefaultInstance, SetSqlQueryAllInstances, SetSqlQuerySpecificInstance, SetFileSystemFile, SetScript, SetXPathQuery
Aliases:

Required: False
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

### -IncludeSubfolder

Indicates whether the cmdlet includes subfolders in the operation.

```yaml
Type: Boolean
Parameter Sets: SetFileSystem, SetFileSystemFile, SetXPathQuery
Aliases: IncludeSubfolders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceName

Specifies the name of a database instance that the global condition searches.
To search the default instance, specify the *UseDefaultInstance* parameter.
To search all instances, specify the *UseAllInstances* parameter.

```yaml
Type: String
Parameter Sets: SetSqlQuerySpecificInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Is64Bit

Indicates that the global condition searches the 64-bit system file location in addition to the 32-bit system file location.

```yaml
Type: Boolean
Parameter Sets: SetFileSystem, SetFileSystemFile, SetXPathQuery, SetRegistryKey, SetRegistryValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyName

Specifies the registry key name for which to search.
Use the format key\subkey.

```yaml
Type: String
Parameter Sets: SetRegistryKey, SetRegistryValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapFilter

Specifies a Lightweight Directory Access Protocol (LDAP) filter to refine the results from the AD DS query to assess compliance on client computers.

```yaml
Type: String
Parameter Sets: SetADQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapPrefix

Specifies a valid LDAP prefix for the AD DS query that assesses compliance on client computers.
The acceptable values for this parameter are: LDAP:// or GC://.

```yaml
Type: String
Parameter Sets: SetADQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MetabasePath

Specifies the path to the metabase file for Internet Information Services (IIS).

```yaml
Type: String
Parameter Sets: SetIisMetabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies the name of the global conditions.
This value corresponds to the **LocalizedDisplayName** property of a global condition object.

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

### -Namespace

Specifies a namespace from a WMI repository.
The default value is Root\cimv2.

```yaml
Type: String
Parameter Sets: SetWqlQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specifies a new name for the global condition.

```yaml
Type: String
Parameter Sets: SetGeneral
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OmaUri

Specifies a Uniform Resource Indicator (URI) that points to device-specific parameters for an Open Mobile Alliance (OMA) device.

```yaml
Type: String
Parameter Sets: SetOmaUri
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

Specifies the path for an OMA URI.

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

### -Property

Specifies the property of the AD DS object used to assess compliance on client computers.

```yaml
Type: String
Parameter Sets: SetWqlQuery, SetADQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyId

Specifies the property of AD DS that Configuration Manager uses to determine client compliance.

```yaml
Type: String
Parameter Sets: SetIisMetabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryHive

Specifies the root key in the registry that identifies the registry hive that you search.
WMI uses the registry hive to return, set, and change the values of registry keys.
The acceptable values for this parameter are:

- ClassesRoot
- CurrentConfig
- CurrentUser
- LocalMachine
- Users

```yaml
Type: RegistryRootKey
Parameter Sets: SetRegistryKey, SetRegistryValue
Aliases:
Accepted values: ClassesRoot, CurrentConfig, CurrentUser, LocalMachine, Users

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptLanguage

Specifies a scripting language to use.
The acceptable values for this parameter are:

- PowerShell
- VBScript
- JScript

```yaml
Type: ScriptingLanguage
Parameter Sets: SetScript
Aliases:
Accepted values: PowerShell, VBScript, JScript, ShellScript

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchScope

Specifies the search scope in AD DS.
The acceptable values for this parameter are:

- Base
- OneLevel
- Subtree

```yaml
Type: SearchScope
Parameter Sets: SetADQuery
Aliases:
Accepted values: Base, OneLevel, Subtree

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Use32BitHost

Indicates that the file or folder is associated with a 64-bit application.

```yaml
Type: Boolean
Parameter Sets: SetScript
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseAllInstances

Indicates that the global condition searches all database instances.
To search a named instance, specify the *InstanceName* parameter.
To search the default instance, specify the *UseDefaultInstance* parameter.

```yaml
Type: SwitchParameter
Parameter Sets: SetSqlQueryAllInstances
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDefaultInstance

Indicates that the global condition searches the default database instance.
To search a named instance, specify the *InstanceName* parameter.
To search all instances, specify the *UseAllInstances* parameter.

```yaml
Type: SwitchParameter
Parameter Sets: SetSqlQueryDefaultInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseLoggedOnUserCredential

Indicates whether to use logged on user credentials.

```yaml
Type: Boolean
Parameter Sets: SetScript
Aliases: UseLoggedOnUserCredentials

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueName

Specifies the value to be contained in the specified registry key.

```yaml
Type: String
Parameter Sets: SetRegistryValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhereClause

Specifies a WQL query WHERE clause to apply to the specified namespace, class, and property on client computers.

```yaml
Type: String
Parameter Sets: SetWqlQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XmlFilePath

Specifies a file that contains the XML query to use to assess compliance on client computers.

```yaml
Type: String
Parameter Sets: SetXPathQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XmlNamespace

Specifies an array of valid, full XML path language (XPath) queries to use to assess compliance on client computers.

```yaml
Type: String[]
Parameter Sets: SetXPathQuery
Aliases: XmlNamespaces

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XPathQuery

Specifies a XPath query.

```yaml
Type: String
Parameter Sets: SetXPathQuery
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

### System.Object
## NOTES

## RELATED LINKS

[New-CMGlobalCondition](./Get-CMGlobalCondition.md)

[Get-CMGlobalCondition](./Set-CMGlobalCondition.md)

[Remove-CMGlobalCondition](./Remove-CMGlobalCondition.md)

[Set-CMGlobalCondition](./Set-CMGlobalCondition.md)

[Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)

[Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)

[Set-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)

[Set-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)

[Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)

[Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)

[Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)

[Set-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)

[Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)

[Set-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXPathQuery.md)
