---
description: Gets Configuration Manager hardware requirements for products.
external help file: AdminUI.PS.dll-Help.xml
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
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

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


