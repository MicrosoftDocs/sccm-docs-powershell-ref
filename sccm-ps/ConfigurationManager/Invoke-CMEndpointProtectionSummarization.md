---
description: Retrieves summary status data about Endpoint Protection.
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Invoke-CMEndpointProtectionSummarization
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

For more information about configuring and monitoring Endpoint Protection, see [How To Monitor Endpoint Configuration In Configuration Manager](https://go.microsoft.com/fwlink/?linkid=268428) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Invoke summarization for Endpoint Protection
```
PS XYZ:\>Invoke-CMEndpointProtectionSummarization -Confirm
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[How To Monitor Endpoint Configuration In Configuration Manager](https://go.microsoft.com/fwlink/?linkid=268428)

[Get-CMEndpointProtectionSummarizationSchedule](Get-CMEndpointProtectionSummarizationSchedule.md)

[Set-CMEndpointProtectionSummarizationSchedule](Set-CMEndpointProtectionSummarizationSchedule.md)


