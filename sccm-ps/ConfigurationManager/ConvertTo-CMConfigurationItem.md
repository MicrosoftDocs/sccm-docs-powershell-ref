---
description: Convert a Configuration Manager management iResultObject to a configuration item object.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/29/2018
schema: 2.0.0
title: ConvertTo-CMConfigurationItem
---

# ConvertTo-CMConfigurationItem

## SYNOPSIS

Convert a Configuration Manager management iResultObject to a configuration item object.

## SYNTAX

### ByObjectValue (Default)
```
ConvertTo-CMConfigurationItem -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByStringValue
```
ConvertTo-CMConfigurationItem -DigestText <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **ConvertTo-CMConfigurationItem** cmdlet converts a string which contains Configuration Item digest XML definition into a ConfigurationItem object.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> $myCI = ConvertTo-CMConfigurationItem -DigestText $digestString
PS XYZ:\> $myCI.Persist($myCI)
```

This command converts a digest into a ConfigurationItem object, and then save the object to the site.

## PARAMETERS

### -DigestText

Specifies the Digest text.

```yaml
Type: String
Parameter Sets: ByStringValue
Aliases:

Required: True
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

### -Force

Forces the command to run without asking for user confirmation.

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

### -InputObject

Specifies a configuration item object.
To obtain a configuration item object, you can use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByObjectValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
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

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)
