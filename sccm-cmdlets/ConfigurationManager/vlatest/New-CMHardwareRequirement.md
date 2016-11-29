---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833691
schema: 2.0.0
ms.assetid: 17573093-E2AE-4B48-8B64-2A239FBA3FC5
---

# New-CMHardwareRequirement

## SYNOPSIS
Creates a Configuration Manager hardware requirement object for a product.

## SYNTAX

```
New-CMHardwareRequirement -Product <String> -MinCpu <Int32> -MinDiskFree <Int64> -MinDiskSize <Int64>
 -MinRam <Int64> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMHardwareRequirement** cmdlet creates a hardware requirement object for a product.

Microsoft System Center Configuration Manager manages Asset Intelligence information, including hardware requirements, for different software products.
You can add, modify, or delete your own hardware requirements, but you cannot change built-in hardware requirement objects.

## EXAMPLES

### Example 1: Create a hardware requirement object
```
PS C:\>New-CMHardwareRequirement -MinCpu 233 -MinDiskFree 1572864 -MinDiskSize 10485760 -MinRam 131072 -Product "Accounts Program"


IsLocal     : 
MinCPU      : 233
MinDiskFree : 1572864
MinDiskSize : 10485760
MinRAM      : 131072
Product     : Accounts Program
State       :
```

This command creates a hardware requirement object for a software product called Accounts Program.
The command specifies the minimum hardware requirements for the product.
If you do not include all of these required parameters, the system prompts you for values.

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

### -MinCpu
Specifies the minimum CPU speed, in megahertz (MHz), required for a software product.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinDiskFree
Specifies the minimum amount of available disk memory, in kilobytes (KB), required for a software product.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinDiskSize
Specifies the minimum disk size, in kilobytes, required for a software product.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinRam
Specifies the minimum amount of random access memory (RAM), in kilobytes, required for a software product.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMHardwareRequirement](./Get-CMHardwareRequirement.md)

[Remove-CMHardwareRequirement](./Remove-CMHardwareRequirement.md)

[Set-CMHardwareRequirement](./Set-CMHardwareRequirement.md)


