---
description: Gets a dependency for a migration entity in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMMigrationEntityDependency
---

# Get-CMMigrationEntityDependency

## SYNOPSIS
Gets a dependency for a migration entity in Configuration Manager.

## SYNTAX

### SearchById (Default)
```
Get-CMMigrationEntityDependency [-Id <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByType
```
Get-CMMigrationEntityDependency [-Type <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMigrationEntityDependency** cmdlet gets a migration entity dependency in Configuration Manager.
A migration entity dependency is an object upon which another object to be migrated is dependent.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get information about all migration entity dependencies
```
PS XYZ:\> Get-CMMigrationEntityDependency
```

This command returns information about all your migration entity dependencies.

### Example 2: Get information about a specific migration entity dependency
```
PS XYZ:\> Get-CMMigrationEntityDependency -Id "121989"
```

This command returns information about the migration entity dependency that has the ID 121989.

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

### -Id
Specifies an ID in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: EntityId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Specifies a type in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByType
Aliases: DependencyType

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

### IResultObject[]#SMS_MigrationEntityDependency
### IResultObject#SMS_MigrationEntityDependency
## NOTES

## RELATED LINKS
