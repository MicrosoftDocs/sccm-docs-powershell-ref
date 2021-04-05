---
description: Imports Configuration Manager configuration items.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/29/2018
schema: 2.0.0
title: Import-CMConfigurationItem
---

# Import-CMConfigurationItem

## SYNOPSIS

Imports Configuration Manager configuration items.

## SYNTAX

```
Import-CMConfigurationItem [-DuplicateWhileImporting] -FileName <String[]> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Import-CMConfigurationItem** cmdlet imports Configuration Manager configuration items from one or more cabinet files.
The files that you import must conform to the Service Modeling Language (SML) schema and can contain information about configuration data from one of the following sources:

- Best practices from a Configuration Manager Configuration Pack.
- Configuration data that you have externally authored and packaged into a cabinet (.cab) file.
- Configuration data exported from Configuration Manager.

Configuration items contain one or more settings, along with compliance rules.
Items usually define a unit of configuration you want to monitor.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import configuration items

```powershell
PS XYZ:\>Import-CMConfigurationItem -FileName "\\atc-dist-01\Public\CM\AdminUITeam\CIData\7389_OSCI.cab","\\atc-dist-01\Public\CM\AdminUITeam\CIData\7452OS_1.cab"
```

This command imports configuration items from the files 7389_OSCI.cab and 7452OS_1.cab.

### Example 2: Import configuration items and create duplicate configuration items

```powershell
PS XYZ:\>Import-CMConfigurationItem -FileName "\\Contoso01\Public\CM\7389_OSCI.cab","\\ Contoso01\Public\CM\7452OS_1.cab" -DuplicateWhileImporting
```

This command imports configuration items from the files 7389_OSCI.cab and 7452OS_1.cab.
The *DuplicateWhileImporting* parameter indicates that imports configuration items that exist in Configuration Manager as duplicate configuration items.

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

### -DuplicateWhileImporting

Indicates that Configuration Manager imports configuration items that exist in Configuration Manager as duplicate configuration items.

Use this parameter to create a configuration item when you want an exact copy of a configuration item that you import to use as your starting point, but you want to modify it to create an independent configuration item from the original.

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

### -FileName

Specifies an array of names of cabinet (cab) files.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Forces the command to run without asking for user confirmation.

Use this parameter to create a configuration item when you want an exact copy of a configuration item that you import to use as your starting point, but you want to modify it to create an independent configuration item from the original.

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

Use this parameter to create a configuration item when you want an exact copy of a configuration item that you import to use as your starting point, but you want to modify it to create an independent configuration item from the original.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Introduction to Compliance Settings in Configuration Manager](/mem/configmgr/compliance/understand/ensure-device-compliance)

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](Get-CMConfigurationItemXMLDefinition.md)

[Get-CMConfigurationItemHistory](Get-CMConfigurationItemHistory.md)

[New-CMConfigurationItem](New-CMConfigurationItem.md)

[Set-CMConfigurationItem](Set-CMConfigurationItem.md)

[Remove-CMConfigurationItem](Remove-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertTo-CMConfigurationItem](ConvertTo-CMConfigurationItem.md)

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)
