---
author: mumian
description:
external help file: AdminUI.PS.Dcm.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: jgao
ms.date: 11/29/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
schema: 2.0.0
title: ConvertFrom-CMConfigurationItem
titleSuffix: Configuration Manager
---

# ConvertFrom-CMConfigurationItem

## SYNOPSIS

Converts a Configuration Manager configuration item to a string.

## SYNTAX

```
ConvertFrom-CMConfigurationItem [-ConfigurationItem] <ConfigurationItem> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **ConvertFrom-CMConfigurationItem** cmdlet converts a ConfigurationItem object into a string which contains the XML definition of the ConfigurationItem object.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

## PARAMETERS

### -ConfigurationItem

Specifies a configuration item.

```yaml
Type: ConfigurationItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.DesiredConfigurationManagement.ConfigurationItem

## OUTPUTS

### System.String

## NOTES

## RELATED LINKS

[Introduction to Compliance Settings in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=211014)

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](Get-CMConfigurationItemXMLDefinition.md)

[Get-CMConfigurationItemHistory](Get-CMConfigurationItemHistory.md)

[New-CMConfigurationItem](New-CMConfigurationItem.md)

[Set-CMConfigurationItem](Set-CMConfigurationItem.md)

[Remove-CMConfigurationItem](Remove-CMConfigurationItem.md)

[Import-CMConfigurationItem](Import-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertTo-CMConfigurationItem](ConvertTo-CMConfigurationItem.md)
