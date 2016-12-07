---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834101
schema: 2.0.0
ms.assetid: EC3D7A25-AFDB-40BE-88E5-3B6506920E8D
---

# Invoke-CMBaselineSummarization

## SYNOPSIS
Updates configuration baseline data.

## SYNTAX

```
Invoke-CMBaselineSummarization [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMBaselineSummarization** cmdlet updates data in configuration baselines in Microsoft System Center Configuration Manager with the latest data from the site database.
This action might take several minutes to complete.

You can use the [Set-CMBaselineSummarizationSchedule](./Set-CMBaselineSummarizationSchedule.md) cmdlet to configure a schedule by which the data is updated with the latest information from the site database.

## EXAMPLES

### Example 1: Update configuration baseline data
```
PS C:\>Invoke-CMBaselineSummarization
```

This command updates data in configuration baselines with the latest data from the site database.

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

[Set-CMBaselineSummarizationSchedule](./Set-CMBaselineSummarizationSchedule.md)

[Get-CMBaselineSummarizationSchedule](./Get-CMBaselineSummarizationSchedule.md)


