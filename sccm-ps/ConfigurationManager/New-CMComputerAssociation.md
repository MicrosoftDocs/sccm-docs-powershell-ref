---
description: Creates an association between two computers in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMComputerAssociation
---

# New-CMComputerAssociation

## SYNOPSIS
Creates an association between two computers in Configuration Manager.

## SYNTAX

```
New-CMComputerAssociation -DestinationComputer <String> [-MigrationBehavior <MigrationBehavior>]
 [-MigrationUserName <String[]>] -SourceComputer <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMComputerAssociation** cmdlet creates an association between two computers to use for migration.
Configuration Manager can migrate user state and settings from an existing computer to a different computer as part of operating system deployment.
In the course of migration, Configuration Manager saves accounts created on the source computer and creates those user accounts on the destination computer.

To create an association, specify the source computer, the destination computer, and at least one user name created on the source computer to be migrated.
You can also specify whether the migration includes other user names from the source computer.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a computer association
```
PS XYZ:\> New-CMComputerAssociation -SourceComputer "TSQA073" -MigrationUserName "Contoso-TSQA\ElisaDaugherty" -DestinationComputer "TSQA155"
```

This command creates a computer association between the source computer named TSQA073 and the destination computer named TSQA155.
The command specifies a user name for migration to the destination computer.

## PARAMETERS

### -DestinationComputer
Specifies the name of a destination computer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RestoreName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -MigrationBehavior
Specifies how Configuration Manager treats user accounts created on the source computer.
When you create a computer association, specify user accounts created on the source computer by using the *MigrationUserName* parameter.
The computer association can specify that the migration process creates some or all of those accounts on the destination computer.

The acceptable values for this parameter are:

- CaptureAllUserAccountsAndRestoreSpecifiedAccounts.
Saves all accounts created on the source computer, but creates only the specified accounts on the destination computer.
- CaptureAndRestoreAllUserAccounts.
Saves all accounts created on the source computer, and creates them on the destination computer.
- CaptureAndRestoreSpecifiedUserAccounts.
Saves only the specified accounts from the source computer, and creates those accounts on the destination computer.

If you do not specify a migration behavior, the migration uses CaptureAndRestoreAllUserAccounts.

```yaml
Type: MigrationBehavior
Parameter Sets: (All)
Aliases:
Accepted values: CaptureAndRestoreAllUserAccounts, CaptureAllUserAccountsAndRestoreSpecifiedAccounts, CaptureAndRestoreSpecifiedUserAccounts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationUserName
Specifies an array of user names for accounts created on the source computer.
The specified user names, along with the *MigrationBehavior* parameter setting, determine which user accounts Configuration Manager creates on the destination computer.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceComputer
Specifies the name of the source computer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceName

Required: True
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_StateMigration

## NOTES

## RELATED LINKS

[Get-CMComputerAssociation](Get-CMComputerAssociation.md)

[Remove-CMComputerAssociation](Remove-CMComputerAssociation.md)

[Set-CMComputerAssociation](Set-CMComputerAssociation.md)


