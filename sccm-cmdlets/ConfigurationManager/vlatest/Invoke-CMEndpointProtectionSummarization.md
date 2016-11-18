---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 0D61AE1F-9859-481D-AF56-E7724212CC22
---

# Invoke-CMEndpointProtectionSummarization

## SYNOPSIS
Retrieves summary status data about Endpoint Protection.

## SYNTAX

```
Invoke-CMEndpointProtectionSummarization [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMEndpointProtectionSummarization** cmdlet retrieves summary status data about System Center 2016 Endpoint Protection in Microsoft System Center Configuration Manager.
This data helps you monitor Endpoint Protection in your System Center Configuration Manager hierarchy.

For more information about configuring and monitoring Endpoint Protection, see [How To Monitor Endpoint Configuration In Configuration Manager](http://go.microsoft.com/fwlink/?linkid=268428) on TechNet.

## EXAMPLES

### Example 1: Invoke summarization for Endpoint Protection
```
PS C:\>Invoke-CMEndpointProtectionSummarization -Confirm
```

This command gets summary data about Endpoint Protection status after you confirm that you want to run the command.

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

[How To Monitor Endpoint Configuration In Configuration Manager](http://go.microsoft.com/fwlink/?linkid=268428)

[Get-CMEndpointProtectionSummarizationSchedule](./Get-CMEndpointProtectionSummarizationSchedule.md)

[Set-CMEndpointProtectionSummarizationSchedule](./Set-CMEndpointProtectionSummarizationSchedule.md)


