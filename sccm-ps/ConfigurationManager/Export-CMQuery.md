---
description: Export a query from Configuration Manager.
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/06/2020
schema: 2.0.0
title: Export-CMQuery
---

# Export-CMQuery

## SYNOPSIS

Export a query from Configuration Manager.

## SYNTAX

### SearchByNameMandatory (Default)
```
Export-CMQuery [-Comment <String>] -ExportFilePath <String> -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Export-CMQuery [-Comment <String>] -ExportFilePath <String> -Id <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Export-CMQuery [-Comment <String>] -ExportFilePath <String> [-InputObject] <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Export-CMQuery** cmdlet exports a query from Configuration Manager. Queries define and store the criteria for sets of database objects that you want to find. For more information, see [Introduction to queries in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-queries).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This command exports a query called **My Systems** to an exported file called **Query.mof**.

```powershell
Export-CMQuery -Name "My Systems" -ExportFilePath "C:\Export\Query.mof"
```

## PARAMETERS

### -Comment

Add a comment to the exported MOF file. For example:



Export-CMQuery -Name "My Systems" -ExportFilePath "C:\Export\Query.mof" -Comment "This is a comment"

This example sets the following comment in the exported file:



// Comments :
//
// This is a comment

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ExportFilePath

Specify the path to the exported file. The file extension is **.mof**.

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

Specify the ID of the query to export. For example, `XYZ00006`.

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

### -InputObject

Specify a query object to export.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Query

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the query to export.

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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Import-CMQuery](Import-CMQuery.md)

[Get-CMQuery](Get-CMQuery.md)

[Invoke-CMQuery](Invoke-CMQuery.md)

[New-CMQuery](New-CMQuery.md)

[Remove-CMQuery](Remove-CMQuery.md)

[Set-CMQuery](Set-CMQuery.md)
