---
description: Gets Configuration Manager status message queries or displays messages.
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
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
Get-CMStatusMessageQuery [-Name <String>] [-ShowMessage] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMStatusMessageQuery -Id <String> [-ShowMessage] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMStatusMessageQuery** cmdlet gets Microsoft System Center Configuration Manager status message queries.
Status message queries return status messages from a System Center Configuration Manager site database.
You can use this cmdlet with the *ShowMessages* parameter to display messages found by this query.

You can use this cmdlet to get queries to use with the [Set-CMStatusMessageQuery](Set-CMStatusMessageQuery.md) cmdlet or the [Remove-CMStatusMessageQuery](Remove-CMStatusMessageQuery.md) cmdlet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

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
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

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
