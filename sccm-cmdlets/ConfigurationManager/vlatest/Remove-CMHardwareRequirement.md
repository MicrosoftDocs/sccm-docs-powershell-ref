---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: C4F9B9A3-3D8E-49EC-9B36-6272EAE7F3C8
---

# Remove-CMHardwareRequirement

## SYNOPSIS
Removes Configuration Manager hardware requirement objects for products.

## SYNTAX

### SearchByNameMandatory (Default)
```
Remove-CMHardwareRequirement -Product <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMHardwareRequirement -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMHardwareRequirement** cmdlet removes hardware requirement objects from Microsoft System Center Configuration Manager.

System Center Configuration Manager manages Asset Intelligence information, including hardware requirements, for different software products.
You can add, modify, or delete your own hardware requirements, but you cannot change built-in hardware requirement objects.

You can use this cmdlet to remove hardware requirement objects.
You can specify a product by name or obtain a requirement by using the **Get-CMHardwareRequirement** cmdlet.

## EXAMPLES

### Example 1: Remove a hardware requirement
```
PS C:\>Remove-CMHardwareRequirement -Product "Accounts Program"
Remove
Are you sure you wish to remove HardwareRequirement: Product="Accounts Program"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

This command removes the hardware requirement object for a product named Accounts Program.

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

### -Force
Performs the action without a confirmation message.

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

### -InputObject
Specifies a hardware requirement object.
To obtain a hardware requirement object, use the **Get-CMHardwareRequirement** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Product
Specifies the name of a software product name.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

[New-CMHardwareRequirement](./New-CMHardwareRequirement.md)

[Set-CMHardwareRequirement](./Set-CMHardwareRequirement.md)


