---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
ms.assetid: 7CA627FC-5C81-490A-B347-045E955DCEA4
online version: https://go.microsoft.com/fwlink/?linkid=834000
schema: 2.0.0
---

# Remove-CMConditionalAccessPolicy

## SYNOPSIS
Removes a conditional access policy.

## SYNTAX

```
Remove-CMConditionalAccessPolicy [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMConditionalAccessPolicy** cmdlet removes a conditional access policy from a Microsoft Configuration Manager site system server.

## EXAMPLES

### Example 1: Remove a conditional access policy by using the pipeline
```
PS C:\> Get-CMConditionalAccessPolicy | Remove-CMConditionalAccessPolicy
```

This command gets the conditional access policy object and uses the pipeline operator to pass the object to **Remove-CMConditionalAccessPolicy**, which removes the conditional access policy.

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
Specifies a conditional access policy object.
To obtain a conditional access policy object, use the Get-CMConditionalAccessPolicy cmdlet.

```yaml
Type: IResultObject
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMConditionalAccessPolicy](Get-CMConditionalAccessPolicy.md)

[New-CMConditionalAccessPolicy](New-CMConditionalAccessPolicy.md)

[Set-CMConditionalAccessPolicy](Set-CMConditionalAccessPolicy.md)


