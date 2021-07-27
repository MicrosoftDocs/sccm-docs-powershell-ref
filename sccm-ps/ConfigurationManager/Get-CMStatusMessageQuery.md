---
description: Gets Configuration Manager status message queries or displays messages.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMStatusMessageQuery
---

# Get-CMStatusMessageQuery

## SYNOPSIS
Gets Configuration Manager status message queries or displays messages.

## SYNTAX

### SearchByName (Default)
```
Get-CMStatusMessageQuery [-Name <String>] [-PassThru] [-ShowMessage] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMStatusMessageQuery -Id <String> [-PassThru] [-ShowMessage] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMStatusMessageQuery** cmdlet gets Configuration Manager status message queries.
Status message queries return status messages from a Configuration Manager site database.
You can use this cmdlet with the *ShowMessages* parameter to display messages found by this query.

You can use this cmdlet to get queries to use with the [Set-CMStatusMessageQuery](Set-CMStatusMessageQuery.md) cmdlet or the [Remove-CMStatusMessageQuery](Remove-CMStatusMessageQuery.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a query that has a specified name
```
PS XYZ:\> Get-CMStatusMessageQuery -Name "Clients That Received a Specific Deployed Program"
```

This command gets a query that has a specified name.

### Example 2: Show messages for a query
```
PS XYZ:\> Get-CMStatusMessageQuery -Id "SMS551" -ShowMessages
```

This command shows messages found by a query that has an ID of SMS551.

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

### -Id
Specifies an ID of a status message query.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: QueryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name of a status message query.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -ShowMessage
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ShowMessages

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_Query
### IResultObject#SMS_Query
## NOTES

## RELATED LINKS

[New-CMStatusMessageQuery](New-CMStatusMessageQuery.md)

[Remove-CMStatusMessageQuery](Remove-CMStatusMessageQuery.md)

[Set-CMStatusMessageQuery](Set-CMStatusMessageQuery.md)
