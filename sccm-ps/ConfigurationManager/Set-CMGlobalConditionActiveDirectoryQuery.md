---
description: Sets an Active Directory Query type global condition in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/07/2019
schema: 2.0.0
title: Set-CMGlobalConditionActiveDirectoryQuery
---

# Set-CMGlobalConditionActiveDirectoryQuery

## SYNOPSIS

Sets an Active Directory Query type global condition in Configuration Manager.

## SYNTAX

```
Set-CMGlobalConditionActiveDirectoryQuery [-DistinguishedName <String>] [-LdapFilter <String>]
 [-LdapPrefix <String>] [-Property <String>] [-SearchScope <SearchScope>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMGlobalConditionActiveDirectoryQuery** cmdlet modifies settings for an Active Directory Query global condition in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> $GlobalQuery = Set-CMGlobalConditionActiveDirectoryQuery -Name GC1 -DataType String -DistinguishedName "CN=Users" -LdapPrefix "LDAP://" -LdapFilter "DC=Vlan123DOM" -Property "DC=net" -SearchScope Base -Description $String
```

This command sets an Active Directory Query type global condition in Configuration Manager.

## PARAMETERS

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

Specifies a distinguished name.

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

### -LdapFilter

Specifies a LDAP filter to refine the results from the Active Directory Domain Services query to assess compliance on client computers.

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

### -LdapPrefix

Specifies a valid LDAP prefix to the Active Directory Domain Services query to assess compliance on client computers. You can use either LDAP:// or GC://.

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

Specifies a name for the Active Directory Query global condition.

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

### -Property

Specifies the property of the Active Directory Domain Services object that will be used to assess compliance on client computers.

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

### -SearchScope

Specifies the search scope in Active Directory Domain Services:

- **Base** - Queries only the specified object.
- **One Level** - This option is not used in this version of Configuration Manager.
- **Subtree** - Queries the specified object and its complete subtree in the directory.

```yaml
Type: SearchScope
Parameter Sets: (All)
Aliases:
Accepted values: Base, OneLevel, Subtree

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMGlobalConditionActiveDirectoryQuery](./New-CMGlobalConditionActiveDirectoryQuery.md)

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
