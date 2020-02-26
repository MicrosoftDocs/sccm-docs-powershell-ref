---
description: Releases locks to global objects in Configuration Manager.
external help file: AdminUI.PS.Common.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Unlock-CMObject
---

# Unlock-CMObject

## SYNOPSIS
Releases locks to global objects in Configuration Manager.

## SYNTAX

```
Unlock-CMObject [-InputObject] <IResultObject[]> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Unlock-CMObject** cmdlet releases locks of one or more objects in Microsoft System Center Configuration Manager.
You can use the *InputObject* parameter to specify the input to this cmdlet, or you can pipe the input to this cmdlet.
When you obtain the lock, the lock is assigned to you, your computer and the site in which the computer resides.
While the lock is assigned to you, no other user or computer can edit the object until you release the lock.

**Important:** Configuration Manager cmdlets now automatically handle the locking and unlocking of objects. Therefore, we do not recommend you use this cmdlet to unlock objects because this may interfere with the functionality of the cmdlets.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Unlock a global object
```
PS XYZ:\> $CIObj = Get-CMDriverPackage -Id "CM100042"
PS XYZ:\> Unlock-CMObject $CIObj
```

The first command gets the driver package object that has the ID CM100042, and stores the object in the $CIObj variable.

The second command releases the lock the object in $CIObj.

## PARAMETERS

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

### -Force
Forces the command to run without asking for user confirmation.

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

### -InputObject
Specifies an array of Configuration Manager objects output from another cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Lock-CMObject](Lock-CMObject.md)

[Move-CMObject](Move-CMObject.md)
