---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833862
schema: 2.0.0
ms.assetid: 6B31564C-A6FC-4D4D-83D6-12EA9BEFC07A
---

# Set-CMGlobalCondition

## SYNOPSIS
Modifies settings for a Configuration Manager global condition.

## SYNTAX

### SetGeneral (Default)
```
Set-CMGlobalCondition -Name <String> [-NewName <String>] [-Description <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetADQuery
```
Set-CMGlobalCondition -Name <String> [-LdapPrefix <String>] [-DistinguishedName <String>]
 [-LdapFilter <String>] [-SearchScope <SearchScope>] [-Property <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetWqlQuery
```
Set-CMGlobalCondition -Name <String> [-Property <String>] [-Namespace <String>] [-Class <String>]
 [-WhereClause <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetAssembly
```
Set-CMGlobalCondition -Name <String> [-AssemblyName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetFileSystem
```
Set-CMGlobalCondition -Name <String> [-Path <String>] [-FileOrFolderName <String>]
 [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetFileSystemFile
```
Set-CMGlobalCondition -Name <String> [-FilePath <String>] [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetScript
```
Set-CMGlobalCondition -Name <String> [-FilePath <String>] [-ScriptLanguage <ScriptingLanguage>]
 [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetXPathQuery
```
Set-CMGlobalCondition -Name <String> [-FilePath <String>] [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 [-XmlFilePath <String>] [-XPathQuery <String>] [-XmlNamespace <String[]>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetSqlQueryDefaultInstance
```
Set-CMGlobalCondition -Name <String> [-FilePath <String>] [-UseDefaultInstance] [-Database <String>]
 [-Column <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetSqlQuerySpecificInstance
```
Set-CMGlobalCondition -Name <String> [-FilePath <String>] [-InstanceName <String>] [-Database <String>]
 [-Column <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetSqlQueryAllInstances
```
Set-CMGlobalCondition -Name <String> [-FilePath <String>] [-UseAllInstances] [-Database <String>]
 [-Column <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRegistryValue
```
Set-CMGlobalCondition -Name <String> [-Is64Bit <Boolean>] [-RegistryHive <RegistryRootKey>] [-KeyName <String>]
 [-ValueName <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetRegistryKey
```
Set-CMGlobalCondition -Name <String> [-Is64Bit <Boolean>] [-RegistryHive <RegistryRootKey>] [-KeyName <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetIisMetabase
```
Set-CMGlobalCondition -Name <String> [-MetabasePath <String>] [-PropertyId <String>] [-PassThru]
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

Microsoft System Center Configuration Manager uses global conditions to represent business or technical conditions.
Global conditions specify how to provide and deploy applications to client devices.

Each global condition must have at least one security scope.

## EXAMPLES

### Example 1: Add a security scope
```
PS C:\>Set-CMGlobalCondition -Name "CPU speed" -SecurityScopeAction AddMembership -SecurityScopeName "Scope22"
```

This command adds the security scope named Scope22 to the global condition named CPU speed.

### Example 2: Remove a security scope by using a variable
```
PS C:\>$CMGC = Get-CMGlobalCondition -Name "CPU speed"
PS C:\> Set-CMGlobalCondition -InputObject $CMGC -SecurityScopeAction RemoveMembership -SecurityScopeName "Scope22"
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
Parameter Sets: SetSqlQueryDefaultInstance, SetSqlQuerySpecificInstance, SetSqlQueryAllInstances
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

### -Database
Specifies the name of a database.
The SQL query runs on this database.

```yaml
Type: String
Parameter Sets: SetSqlQueryDefaultInstance, SetSqlQuerySpecificInstance, SetSqlQueryAllInstances
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
Specifies the name of a file or folder.
Specify the *IsFolder* parameter to search for a folder.

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
Parameter Sets: SetFileSystemFile, SetScript, SetXPathQuery, SetSqlQueryDefaultInstance, SetSqlQuerySpecificInstance, SetSqlQueryAllInstances
Aliases: 
Required: False
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

### -IncludeSubfolder


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
Parameter Sets: SetFileSystem, SetFileSystemFile, SetXPathQuery, SetRegistryValue, SetRegistryKey
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
Parameter Sets: SetRegistryValue, SetRegistryKey
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
This value corresponds to the LocalizedDisplayName property of a global condition object.

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
Returns an object representing the item with which you are working.
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
Parameter Sets: SetADQuery, SetWqlQuery
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
Parameter Sets: SetRegistryValue, SetRegistryKey
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
The acceptable values for this parameter are: PowerShell, VBScript, and JScript.

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
The acceptable values for this parameter are: Base, OneLevel, and Subtree.

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

### -XPathQuery


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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMGlobalCondition](./Get-CMGlobalCondition.md)

[New-CMGlobalCondition](./New-CMGlobalCondition.md)

[Remove-CMGlobalCondition](./Remove-CMGlobalCondition.md)
