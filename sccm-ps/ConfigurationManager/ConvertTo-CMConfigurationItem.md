---
title: ConvertTo-CMConfigurationItem
titleSuffix: Configuration Manager
description: Convert a Configuration Manager management iResultObject to a configuration item object.
ms.date: 11/29/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# ConvertTo-CMConfigurationItem

## SYNOPSIS

Convert a Configuration Manager management iResultObject to a configuration item object.

## SYNTAX

### ByObjectValue (Default)

```powershell
ConvertTo-CMConfigurationItem -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling]
```

### ByStringValue

```powershell
ConvertTo-CMConfigurationItem -DigestText <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

The **ConvertTo-CMConfigurationItem** cmdlet converts a string which contains Configuration Item digest XML definition into a ConfigurationItem object.

## EXAMPLES

### Example 1

```powershell
PS C:\> $myCI = ConvertTo-CMConfigurationItem -DigestText $digestString 
PS C:\> $myCI.Persist($myCI)    
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

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## RELATED LINKS

[Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014)

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](Get-CMConfigurationItemXMLDefinition.md)

[Get-CMConfigurationItemHistory](Get-CMConfigurationItemHistory.md)

[New-CMConfigurationItem](New-CMConfigurationItem.md)

[Set-CMConfigurationItem](Set-CMConfigurationItem.md)

[Remove-CMConfigurationItem](Remove-CMConfigurationItem.md)

[Import-CMConfigurationItem](Import-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)