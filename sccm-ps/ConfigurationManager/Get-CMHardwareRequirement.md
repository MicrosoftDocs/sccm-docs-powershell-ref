---
description: Gets Configuration Manager hardware requirements for products.
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMHardwareRequirement
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

Configuration Manager manages Asset Intelligence information, including hardware requirements, for different software products.
You can add, modify, or delete your own hardware requirements, but you cannot change built-in hardware requirement objects.

You can use this cmdlet to get all the hardware requirement objects for a Configuration Manager server or one or more hardware requirement objects for a specified product names.
You can use hardware requirements with other cmdlets, such as the **Remove-CMHardwareRequirement** cmdlet or the **Set-CMHardwareRequirement** cmdlet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_AIHardwareRequirements

### IResultObject#SMS_AIHardwareRequirements

## NOTES

## RELATED LINKS

[New-CMHardwareRequirement](New-CMHardwareRequirement.md)

[Remove-CMHardwareRequirement](Remove-CMHardwareRequirement.md)

[Set-CMHardwareRequirement](Set-CMHardwareRequirement.md)


