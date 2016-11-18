---
external help file: AdminUI.PS.Migration.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: E9057BB2-EFBE-45F9-AF07-71933FF4BB4E
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

## EXAMPLES

### Example 1: Get information about all migration entity dependencies
```
PS C:\>Get-CMMigrationEntityDependency
```

This command returns information about all your migration entity dependencies.

### Example 2: Get information about a specific migration entity dependency
```
PS C:\>Get-CMMigrationEntityDependency -Id "121989"
```

This command returns information about the migration entity dependency that has the ID 121989.

## PARAMETERS

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


