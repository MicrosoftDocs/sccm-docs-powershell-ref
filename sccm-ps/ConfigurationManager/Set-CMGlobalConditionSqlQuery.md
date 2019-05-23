---
title: Set-CMGlobalConditionSqlQuery
titleSuffix: Configuration Manager
description: Sets a SQL Query type global condition in Configuration Manager.
ms.date: 01/08/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Set-CMGlobalConditionSqlQuery

## SYNOPSIS

Sets a SQL Query type global condition in Configuration Manager.

## SYNTAX

### SetQueryFromFile (Default)

```powershell
Set-CMGlobalConditionSqlQuery [-FilePath <String>] [-UseDefaultInstance] [-UseAllInstances]
 [-InstanceName <String>] [-Database <String>] [-Column <String>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

### SetQueryFromText

```powershell
Set-CMGlobalConditionSqlQuery [-QueryText <String>] [-UseDefaultInstance] [-UseAllInstances]
 [-InstanceName <String>] [-Database <String>] [-Column <String>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
```

## DESCRIPTION

The **Set-CMGlobalConditionSqlQuery** cmdlet modifies settings for a SQL Query type global condition in Microsoft System Center Configuration Manager.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1

```powershell
PS XYZ:\> $GlobalSql = Set-CMGlobalConditionSqlQuery -DataType String -QueryText $string -Database ss -Column aa â€“Name GC6
```

This command sets a SQL Query type global condition in Configuration Manager.

## PARAMETERS

### -Column

Specifies the column name returned by the Transact-SQL statement to use to assess the compliance of the global condition.

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

### -Database

Specifies the name of the Microsoft SQL Server database for which the SQL query will be run.

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

### -FilePath

Specifies a file path.

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

### -InstanceName

Specifies a SQL Server instance where you want the SQL Query to run on.

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

### -QueryText

Specifies the full SQL query to use for the global condition. 

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

### -UseAllInstances

Indicates running the SQL query on all instances.

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

### -UseDefaultInstance

Indicates running the SQL query on the default instance.

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

- [New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)
- [Set-CMGlobalCondition](./Set-CMGlobalCondition.md)
- [Set-CMGlobalConditionActiveDirectoryQuery](./Set-CMGlobalConditionActiveDirectoryQuery.md)
- [Set-CMGlobalConditionAssembly](./Set-CMGlobalConditionAssembly.md)
- [Set-CMGlobalConditionFile](./Set-CMGlobalConditionFile.md)
- [Set-CMGlobalConditionIisMetabase](./Set-CMGlobalConditionIisMetabase.md)
- [Set-CMGlobalConditionOmaUri](./Set-CMGlobalConditionOmaUri.md)
- [Set-CMGlobalConditionRegistryKey](./Set-CMGlobalConditionRegistryKey.md)
- [Set-CMGlobalConditionRegistryValue](./Set-CMGlobalConditionRegistryValue.md)
- [Set-CMGlobalConditionScript](./Set-CMGlobalConditionScript.md)
- [Set-CMGlobalConditionWqlQuery](./Set-CMGlobalConditionWqlQuery.md)
- [Set-CMGlobalConditionXPathQuery](./Set-CMGlobalConditionXPathQuery.md)
