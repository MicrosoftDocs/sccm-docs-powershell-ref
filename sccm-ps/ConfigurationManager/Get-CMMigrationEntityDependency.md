---
description: Gets a dependency for a migration entity in Configuration Manager.
external help file: AdminUI.PS.Migration.dll-Help.xml
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
The **Get-CMMigrationEntityDependency** cmdlet gets a migration entity dependency in Microsoft System Center Configuration Manager.
A migration entity dependency is an object upon which another object to be migrated is dependent.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

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
