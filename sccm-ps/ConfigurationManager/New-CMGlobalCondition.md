---
external help file: AdminUI.PS.Dcm.dll-Help.xml
ms.assetid: 69A0D711-0B7F-4877-A2F9-C3CE64CC6698
online version: https://go.microsoft.com/fwlink/?linkid=833687
schema: 2.0.0
---

# New-CMGlobalCondition

## SYNOPSIS
Creates a global condition in Configuration Manager.

## SYNTAX

### NewADQuery (Default)
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> [-LdapPrefix <String>] -DistinguishedName <String> -LdapFilter <String>
 -SearchScope <SearchScope> -Property <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### NewIisMetabase
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> [-MetabasePath <String>] -PropertyId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewRegistryValue
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> [-Is64Bit <Boolean>] -RegistryHive <RegistryRootKey> -KeyName <String>
 -ValueName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewScript
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> -FilePath <String> -ScriptLanguage <ScriptingLanguage>
 [-UseLoggedOnUserCredential <Boolean>] [-Use32BitHost <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewSqlQueryDefaultInstance
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> -FilePath <String> [-DefaultInstance] -Database <String> -Column <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewSqlQueryAllInstances
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> -FilePath <String> [-AllInstances] -Database <String> -Column <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewSqlQuerySpecificInstance
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> -FilePath <String> -InstanceName <String> -Database <String>
 -Column <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewWqlQuery
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> -Property <String> [-Namespace <String>] -Class <String>
 [-WhereClause <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewXPathQuery
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> -FilePath <String> [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 [-XmlNamespace <String[]>] -XPathQuery <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### NewXPathQueryFromFile
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> -FilePath <String> [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 [-XmlNamespace <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewOmaUri
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -DataType <GlobalConditionDataType> -OmaUri <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewAssembly
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -AssemblyName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewFileSystem
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 [-IsFolder] -Path <String> -FileOrFolderName <String> [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewFileSystemFile
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 -FilePath <String> [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewRegistryKey
```
New-CMGlobalCondition -Name <String> [-Description <String>] -DeviceType <GlobalConditionDeviceType>
 [-Is64Bit <Boolean>] -RegistryHive <RegistryRootKey> -KeyName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMGlobalCondition** cmdlet creates a global condition in Microsoft System Center Configuration Manager.
A global condition is a setting or expression in System Center Configuration Manager that you can use to specify how System Center Configuration Manager provides and deploys an application to clients.

## EXAMPLES

### Example 1: Create a global condition
```
PS C:\> New-CMGlobalCondition -AssemblyName "Microsoft.Office.Tools.Word.v9.0" -DeviceType $Windows
```

This command creates a global condition that searches the assembly named Microsoft.Office.Tools.Word.v9.0 on Windows devices.

## PARAMETERS

### -AllInstances
```yaml
Type: SwitchParameter
Parameter Sets: NewSqlQueryAllInstances
Aliases: UseAllInstances

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssemblyName
Specifies the name of an assembly for which to search.
An assembly name must be registered in the Global Assembly Cache.

```yaml
Type: String
Parameter Sets: NewAssembly
Aliases: 

Required: True
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
Parameter Sets: NewWqlQuery
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Column
Specifies the column name used to assess the compliance of the global condition.

```yaml
Type: String
Parameter Sets: NewSqlQueryDefaultInstance, NewSqlQueryAllInstances, NewSqlQuerySpecificInstance
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

### -DataType
Specifies the global condition data type.
The acceptable values for this parameter are:

- Boolean 
- DateTime
- FloatingPoint
- Integer
- IntegerArray 
- String 
- StringArray
- Version

```yaml
Type: GlobalConditionDataType
Parameter Sets: NewADQuery, NewIisMetabase, NewRegistryValue, NewScript, NewSqlQueryDefaultInstance, NewSqlQueryAllInstances, NewSqlQuerySpecificInstance, NewWqlQuery, NewXPathQuery, NewXPathQueryFromFile, NewOmaUri
Aliases: 
Accepted values: String, DateTime, Integer, FloatingPoint, Version, Boolean, StringArray, IntegerArray, Base64, Xml

Required: True
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
Parameter Sets: NewSqlQueryDefaultInstance, NewSqlQueryAllInstances, NewSqlQuerySpecificInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultInstance
```yaml
Type: SwitchParameter
Parameter Sets: NewSqlQueryDefaultInstance
Aliases: UseDefaultInstance

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the global condition.

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

### -DeviceType
Specifies the type of device to which this global condition applies.
The acceptable values for this parameter are: Nokia, Windows, and WindowsMobile.

```yaml
Type: GlobalConditionDeviceType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, WindowsMobile

Required: True
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

### -DistinguishedName
Specifies the distinguished name of the Active Directory Domain Services (AD DS) object to assess for compliance on client computers.

```yaml
Type: String
Parameter Sets: NewADQuery
Aliases: 

Required: True
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
Parameter Sets: NewFileSystem
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
Specifies a file path for the file that the condition assesses for compliance.

```yaml
Type: String
Parameter Sets: NewScript, NewSqlQueryDefaultInstance, NewSqlQueryAllInstances, NewSqlQuerySpecificInstance, NewXPathQuery, NewXPathQueryFromFile, NewFileSystemFile
Aliases: XmlFilePath

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
```yaml
Type: Boolean
Parameter Sets: NewXPathQuery, NewXPathQueryFromFile, NewFileSystem, NewFileSystemFile
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
Parameter Sets: NewSqlQuerySpecificInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Is64Bit
Indicates that the global condition searches the 64-bit system file location in addition to the 32-bit system file location.

```yaml
Type: Boolean
Parameter Sets: NewRegistryValue, NewXPathQuery, NewXPathQueryFromFile, NewFileSystem, NewFileSystemFile, NewRegistryKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsFolder
Indicates that the global condition searches for a folder.
If you do not select this parameter, the condition searches for a file.
Specify the name of the file or folder by using the *FileOrFolderName* parameter.

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

### -KeyName
Specifies the registry key name for which to search.
Use the format key\subkey.

```yaml
Type: String
Parameter Sets: NewRegistryValue, NewRegistryKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapFilter
Specifies a Lightweight Directory Access Protocol (LDAP) filter to refine the results from the AD DS query to assess compliance on client computers.

```yaml
Type: String
Parameter Sets: NewADQuery
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LdapPrefix
Specifies a valid LDAP prefix for the AD DS query that assesses compliance on client computers.
This prefix can be either LDAP:// or GC://.

```yaml
Type: String
Parameter Sets: NewADQuery
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
Parameter Sets: NewIisMetabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of an IIS metabase file.

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
Parameter Sets: NewWqlQuery
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
Parameter Sets: NewOmaUri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the path for an OMA URI.

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

### -Property
Specifies the property of the AD DS object used to assess compliance on client computers.

```yaml
Type: String
Parameter Sets: NewADQuery, NewWqlQuery
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyId
Specifies the property of AD DS that Configuration Manager uses to determine client compliance.

```yaml
Type: String
Parameter Sets: NewIisMetabase
Aliases: 

Required: True
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
Parameter Sets: NewRegistryValue, NewRegistryKey
Aliases: 
Accepted values: ClassesRoot, CurrentConfig, CurrentUser, LocalMachine, Users

Required: True
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
Parameter Sets: NewScript
Aliases: 
Accepted values: PowerShell, VBScript, JScript, ShellScript

Required: True
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
Parameter Sets: NewADQuery
Aliases: 
Accepted values: Base, OneLevel, Subtree

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Use32BitHost
Indicates that the file or folder is associated with a 64-bit application.

```yaml
Type: Boolean
Parameter Sets: NewScript
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
Parameter Sets: NewScript
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
Parameter Sets: NewRegistryValue
Aliases: 

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

### -WhereClause
Specifies a WQL query WHERE clause to apply to the specified namespace, class, and property on client computers.

```yaml
Type: String
Parameter Sets: NewWqlQuery
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
Parameter Sets: NewXPathQuery
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XmlNamespace
Specifies an array of valid, full XML path language (XPath) queries to use to assess compliance on client computers.

```yaml
Type: String[]
Parameter Sets: NewXPathQuery, NewXPathQueryFromFile
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

[Get-CMGlobalCondition](Get-CMGlobalCondition.md)

[Remove-CMGlobalCondition](Remove-CMGlobalCondition.md)

[Set-CMGlobalCondition](Set-CMGlobalCondition.md)
