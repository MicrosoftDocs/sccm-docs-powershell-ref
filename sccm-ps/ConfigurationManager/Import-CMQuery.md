---
description: Import a set of exported queries to Configuration Manager.
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/06/2020
schema: 2.0.0
title: Import-CMQuery
---

# Import-CMQuery

## SYNOPSIS

Import a set of exported queries to Configuration Manager.

## SYNTAX

```
Import-CMQuery [-ImportFilePath] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Import-CMQuery** cmdlet imports a set of exported queries to Configuration Manager. Queries define and store the criteria for sets of database objects that you want to find. For more information, see [Introduction to queries in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-queries).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This command imports a set of queries from an exported file, `C:\Export\Query.mof`.

```powershell
Import-CMQuery -ImportFilePath "C:\Export\Query.nof"
```

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

### -ImportFilePath

Specify the path to the file to import. The file extension is **.mof**.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 0
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

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Export-CMQuery](Export-CMQuery.md)

[Get-CMQuery](Get-CMQuery.md)

[Invoke-CMQuery](Invoke-CMQuery.md)

[New-CMQuery](New-CMQuery.md)

[Remove-CMQuery](Remove-CMQuery.md)

[Set-CMQuery](Set-CMQuery.md)
