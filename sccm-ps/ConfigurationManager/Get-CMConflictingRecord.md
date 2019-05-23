---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
ms.assetid: 5B0C478D-55DA-4A57-9176-47B810CEA35B
online version: https://go.microsoft.com/fwlink/?linkid=834286
schema: 2.0.0
---

# Get-CMConflictingRecord

## SYNOPSIS
Gets conflicting Configuration Manager record objects.

## SYNTAX

### SearchByName (Default)
```
Get-CMConflictingRecord [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMConflictingRecord -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConflictingRecord** cmdlet gets one or more conflicting Microsoft System Center Configuration Manager record objects.

When Configuration Manager recognizes a new client, it uses hardware information to check whether it previously created a record for that computer.
For example, you might have reinstalled the operating system.
The previous client record still exists with the same hardware information.
If you manually resolve conflicts, you have the option to merge the new record with the existing record, create a new record, or create a record as a blocked record.
You can also configure Configuration Manager to resolve conflicts automatically.

You can use this cmdlet with the [Block-CMConflictingRecord](Block-CMConflictingRecord.md) cmdlet or the [Merge-CMConflictingRecord](Merge-CMConflictingRecord.md) cmdlet.
You can get all the outstanding conflicts for Configuration Manager or specify a conflict by name or by ID.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get all conflicting records
```
PS XYZ:\> Get-CMConflictingRecord
```

This command gets all the unresolved conflicts for Configuration Manager.

### Example 2: Get a named conflicting record
```
PS XYZ:\> Get-CMConflictingRecord -Name "CR07"
```

This command gets a conflict named CR07.

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
Specifies an ID for the conflicting records.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: Smsid

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the conflicting records.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: AgentName

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

[Block-CMConflictingRecord](Block-CMConflictingRecord.md)

[Merge-CMConflictingRecord](Merge-CMConflictingRecord.md)
