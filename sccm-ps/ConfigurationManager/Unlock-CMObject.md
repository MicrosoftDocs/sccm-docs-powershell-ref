---
description: Release a SEDO lock on an object.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/05/2021
schema: 2.0.0
title: Unlock-CMObject
---

# Unlock-CMObject

## SYNOPSIS

Release a SEDO lock on an object.

## SYNTAX

```
Unlock-CMObject [-Force] [-InputObject] <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!WARNING]
> Configuration Manager cmdlets automatically lock and unlock objects. Use of this cmdlet may interfere with the functionality of other cmdlets.

The **Unlock-CMObject** cmdlet releases the SEDO lock on one or more objects. Configuration Manager SEDO (Serialized Editing of Distributed Objects) is a mechanism to assign locks to globally replicated objects. If a user wants to edit and save an object, they have to get a lock from the site. The site assigns a lock to the user for that object, on their computer, and in the site. While the user has the lock, no one else can edit the object.

For more information, see [Configuration Manager SEDO](/mem/configmgr/develop/core/understand/sedo).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Unlock a driver package

The first command gets the driver package with the ID **CM100042**, and stores it in the **$CIObj** variable. The second command releases the lock it. The third command shows the details of the lock, which is now blank.

```powershell
$CIObj = Get-CMDriverPackage -Id "CM100042"
Unlock-CMObject $CIObj
Get-CMObjectLockDetails -InputObject $CIObj
```

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

### -InputObject

Specify an array of Configuration Manager objects that are output from another cmdlet. For example, to get an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

For a list of objects that are SEDO-enabled, see [Configuration Manager SEDO](/mem/configmgr/develop/core/understand/sedo).

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Lock-CMObject](Lock-CMObject.md)

[Get-CMObjectLockDetails](Get-CMObjectLockDetails.md)

[Configuration Manager SEDO](/mem/configmgr/develop/core/understand/sedo)
