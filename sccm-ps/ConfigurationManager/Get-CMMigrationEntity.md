---
external help file: AdminUI.PS.Migration.dll-Help.xml
ms.assetid: D02E7E60-2F2E-4EBE-9EB3-CA8CA9914289
online version: https://go.microsoft.com/fwlink/?linkid=833758
schema: 2.0.0
---

# Get-CMMigrationEntity

## SYNOPSIS
Gets a migration entity in System Center Configuration Manager.

## SYNTAX

### SearchById (Default)
```
Get-CMMigrationEntity [-Id <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByName
```
Get-CMMigrationEntity [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByOthers
```
Get-CMMigrationEntity [-Type <String>] [-IsActive <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMigrationEntity** cmdlet gets the migration entity in Microsoft System Center Configuration Manager.
A migration entity is an object to be migrated that is of any type that is supported by migration.

## EXAMPLES

### Example 1: Get information about all your migration entities
```
PS C:\> Get-CMMigrationEntity
```

This command returns information about all of your migration entities.

### Example 2: Get information about a specific migration entity
```
PS C:\> Get-CMMigrationEntity -Name "MigrationTest"
```

This command returns information about the migration entity with the name MigrationTest.

### Example 3: Get information about active migration entities
```
PS C:\> Get-CMMigrationEntity -IsActive
```

This command returns information about all of your active migration entities.

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
Specifies an identifier in Configuration Manager.

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

### -IsActive
Specifies that this migration entity is active.

```yaml
Type: String
Parameter Sets: SearchByOthers
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: EntityName

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
Parameter Sets: SearchByOthers
Aliases: 

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

[Get-CMMigrationEntityDependency](Get-CMMigrationEntityDependency.md)

[New-CMMigrationJob](New-CMMigrationJob.md)


