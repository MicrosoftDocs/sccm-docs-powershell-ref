<<<<<<< HEAD
---
title: Get-CMHardwareRequirement
titleSuffix: Configuration Manager
description: Gets Configuration Manager hardware requirements for products.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
ms.assetid: 64498870-8A44-440C-B6A6-D0D25C3805FE
online version: https://go.microsoft.com/fwlink/?linkid=833714
schema: 2.0.0
>>>>>>> master
---

# Get-CMHardwareRequirement

## SYNOPSIS
Gets Configuration Manager hardware requirements for products.

## SYNTAX

```
Get-CMHardwareRequirement [-Product <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMHardwareRequirement** cmdlet gets hardware requirements objects for software products.

Microsoft System Center Configuration Manager manages Asset Intelligence information, including hardware requirements, for different software products.
You can add, modify, or delete your own hardware requirements, but you cannot change built-in hardware requirement objects.

You can use this cmdlet to get all the hardware requirement objects for a System Center Configuration Manager server or one or more hardware requirement objects for a specified product names.
You can use hardware requirements with other cmdlets, such as the **Remove-CMHardwareRequirement** cmdlet or the **Set-CMHardwareRequirement** cmdlet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get a hardware requirement
```
PS XYZ:\> Get-CMHardwareRequirement -Product "Accounts Program"
IsLocal     : False
MinCPU      : 233
MinDiskFree : 1572864
MinDiskSize : 10485760
MinRAM      : 131072
Product     : Accounts Program
State       : 0
```

This command gets the hardware requirement object for a product named Accounts Program.

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

### -Product
Specifies the name of a software product.

```yaml
Type: String
Parameter Sets: (All)
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

[New-CMHardwareRequirement](New-CMHardwareRequirement.md)

[Remove-CMHardwareRequirement](Remove-CMHardwareRequirement.md)

[Set-CMHardwareRequirement](Set-CMHardwareRequirement.md)


