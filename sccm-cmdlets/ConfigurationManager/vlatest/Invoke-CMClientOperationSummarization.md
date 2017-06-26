---
external help file: AdminUI.PS.ClientOperations.dll-Help.xml
ms.assetid: 33A18314-C3D3-4457-9E93-7D5C3A46D621
online version: https://go.microsoft.com/fwlink/?linkid=834109
schema: 2.0.0
---

# Invoke-CMClientOperationSummarization

## SYNOPSIS
Performs a Configuration Manager client operations summarization.

## SYNTAX

```
Invoke-CMClientOperationSummarization [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMClientOperationSummarization** cmdlet performs a Microsoft System Center Configuration Manager client operations summarization immediately, instead of waiting for the next scheduled summarization.
This cmdlet does not change the regular schedule for summarizations.

## EXAMPLES

### Example 1: Invoke summarization
```
PS C:\>Invoke-CMClientOperationSummarization
```

This command performs a client operations summarization immediately.

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

[Clear-CMClientOperation](./Clear-CMClientOperation.md)

[Remove-CMClientOperation](./Remove-CMClientOperation.md)


