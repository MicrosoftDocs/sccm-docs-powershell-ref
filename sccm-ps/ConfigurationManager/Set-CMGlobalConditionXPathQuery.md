---
title: Set-CMGlobalConditionXPathQuery
titleSuffix: Configuration Manager
description: Sets a XPath Query type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Set-CMGlobalConditionXPathQuery

## SYNOPSIS

Sets a XPath Query type global condition in Configuration Manager.

## SYNTAX

### SetQueryFromFile (Default)

```powershell
Set-CMGlobalConditionXPathQuery [-XmlFilePath <String>] [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 [-XPathQueryFilePath <String>] [-XmlNamespace <String[]>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### SetQueryFromText

```powershell
Set-CMGlobalConditionXPathQuery [-XmlFilePath <String>] [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>]
 [-XPathQuery <String>] [-XmlNamespace <String[]>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

## DESCRIPTION

The **Set-CMGlobalConditionXPathQuery** cmdlet modifies settings for a XPath Query type global condition in Microsoft System Center Configuration Manager.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1

```powershell
PS XYZ:\> $GlobalXpath = Set-CMGlobalConditionXPathQuery -DataType String -XmlFilePath "c:\A" -XPathQuery "/" -Name GC8
```

This command sets a XPath Query type global condition in Configuration Manager.

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

Indicates whether to search any sub-folders under the specified path.

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

Indicate whether the 64-bit system file location (%windir%\system32) should be searched in addition to the 32-bit system file location (%windir%\syswow64) on Configuration Manager clients that run a 64-bit version of Windows.

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

### -XmlFilePath

Specifies the path to the XML file on client computers that will be used to assess compliance. Configuration Manager supports the use of all Windows system environment variables and the %USERPROFILE% user variable in the path name.

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

### -XmlNamespace

Specifies namespaces to use during the XPath query.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: XmlNamespaces

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XPathQuery

Specifies a valid full XML path language (XPath) query to use to assess compliance on client computers.

```yaml
Type: String
Parameter Sets: SetQueryFromText
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -XPathQueryFilePath

Specifies a XPath query file path.

```yaml
Type: String
Parameter Sets: SetQueryFromFile
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

- [New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXPathQuery.md)
- [Set-CMGlobalCondition](./Set-CMGlobalCondition.md)
- [Set-CMGlobalConditionActiveDirectoryQuery](./Set-CMGlobalConditionActiveDirectoryQuery.md)
- [Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)
- [Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)
- [Set-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)
- [Set-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)
- [Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)
- [Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)
- [Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)
- [Set-CMGlobalConditionSqlQuery](./Set-CMGlobalConditionSqlQuery.md)
- [Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)
