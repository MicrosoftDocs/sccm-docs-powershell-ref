---
description: Resolves a conflict in Configuration Manager software inventory information.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Resolve-CMInventoriedSoftwareConflict
---

# Resolve-CMInventoriedSoftwareConflict

## SYNOPSIS
Resolves a conflict in Configuration Manager software inventory information.

## SYNTAX

```
Resolve-CMInventoriedSoftwareConflict -Id <String> -RevertLocalEdit <Boolean> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Resolve-CMInventoriedSoftwareConflict** cmdlet resolves a conflict in Configuration Manager software inventory information.

When Configuration Manager receives updated information about software that is part of the software inventory, that information may conflict with your local settings.
You can resolve a conflict by keeping your local inventory information or updating to the new information.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Resolve a software conflict and keep local inventory information
```
PS XYZ:\> Resolve-CMInventoriedSoftwareConflict -Id "SMS0001" -RevertLocalEdit $True
```

This command resolves a software conflict that has the specified ID.
The command keeps the current, local version of the conflicting information.

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
Specifies an array of IDs for conflicts in software inventory.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SoftwareKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RevertLocalEdit
Indicates whether this cmdlet keeps the current inventory information for the conflict or updates that information.
If this parameter is $True, the cmdlet keeps current, local information.
If this parameter is $False, the cmdlet replaces conflicting information with updated information.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

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

### System.Object
## NOTES

## RELATED LINKS

[Get-CMSoftwareInventory](Get-CMSoftwareInventory.md)

[Set-CMSoftwareInventory](Set-CMSoftwareInventory.md)

[Undo-CMSoftwareInventory](Undo-CMSoftwareInventory.md)


