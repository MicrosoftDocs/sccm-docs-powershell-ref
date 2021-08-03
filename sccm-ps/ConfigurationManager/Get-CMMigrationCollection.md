---
description: Gets collections selected for migration.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMMigrationCollection
---

# Get-CMMigrationCollection

## SYNOPSIS
Gets collections selected for migration.

## SYNTAX

### SearchById (Default)
```
Get-CMMigrationCollection [-Id <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMMigrationCollection [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMigrationCollection** cmdlet gets the collections selected from a source hierarchy for migration.
A collection is a set of resources in the Configuration Manager hierarchy.
A migration collection is the set of resources chosen from a hierarchy for migration, including related objects.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a migration collection by name
```
PS XYZ:\> Get-CMMigrationCollection -Name "PhoneCollection5"
```

This command gets the migration collection.
The command specifies the value PhoneCollection5 for the *Name* parameter.

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
Specifies an identifier for a collection in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: CollectionEntityId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for a collection in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CollectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_MigrationCollectionInfo
### IResultObject#SMS_MigrationCollectionInfo
## NOTES

## RELATED LINKS
