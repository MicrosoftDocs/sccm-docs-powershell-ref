---
description: Creates a status message query.
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMStatusMessageQuery
---

# New-CMStatusMessageQuery

## SYNOPSIS
Creates a status message query.

## SYNTAX

```
New-CMStatusMessageQuery -Name <String> [-Comment <String>] [-Expression <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMStatusMessageQuery** cmdlet creates a status message query in Microsoft System Center Configuration Manager.
Status message queries in System Center Configuration Manager return status messages from the site database.
All major System Center Configuration Manager components generate status messages.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a status message query
```
PS XYZ:\> New-CMStatusMessageQuery -Name "Client Component Configuration Changes and Fatal Errors" -Expression "select stat.*, ins.*, att1.*, stat.Time from SMS_StatusMessage as stat left join SMS_StatMsgInsStrings as ins on stat.RecordID = ins.RecordID left join SMS_StatMsgAttributes as att1 on stat.RecordID = att1.RecordID where stat.ModuleName = 'SMS Client' and stat.MessageID = 669 and stat.SiteCode = ##PRM:SMS_StatusMessage.SiteCode## and stat.Time >= ##PRM:SMS_StatusMessage.Time## order by stat.Time desc"
```

This command creates a status message query named Client Component Configuration Changes and Fatal Errors.
The *Expression* parameter specifies the WMI Query Language (WQL) text for the query.

## PARAMETERS

### -Comment
```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
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

### -Expression
Specifies WMI Query Language (WQL) text for the query.

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

### -Name
Specifies a name for the status message query.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_Query

## NOTES

## RELATED LINKS

[Get-CMStatusMessageQuery](Get-CMStatusMessageQuery.md)

[Set-CMStatusMessageQuery](Set-CMStatusMessageQuery.md)

[Remove-CMStatusMessageQuery](Remove-CMStatusMessageQuery.md)


