---
external help file: AdminUI.PS.Migration.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: ED0B8420-DCA5-43D7-A48B-45A539486580
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
A collection is a set of resources in the Microsoft System Center Configuration Manager hierarchy.
A migration collection is the set of resources chosen from a hierarchy for migration, including related objects.

## EXAMPLES

### Example 1: Get a migration collection by name
```
PS C:\>Get-CMMigrationCollection -Name "PhoneCollection5"
```

This command gets the migration collection.
The command specifies the value PhoneCollection5 for the *Name* parameter.

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
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


