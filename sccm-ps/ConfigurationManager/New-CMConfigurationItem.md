---
title: New-CMConfigurationItem
titleSuffix: Configuration Manager
description: Creates a Configuration Manager configuration item.
ms.date: 11/29/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# New-CMConfigurationItem

## SYNOPSIS

Creates a Configuration Manager configuration item.

## SYNTAX

### NewChild (Default)

```powershell
New-CMConfigurationItem -Name <String> [-Description <String>] [-Category <String[]>]
 -ParentConfigurationItem <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### New

```powershell
New-CMConfigurationItem -Name <String> [-Description <String>] [-Category <String[]>]
 -CreationType <CICreationType> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMConfigurationItem** cmdlet creates a configuration item in Microsoft System Center Configuration Manager.
Create configuration items to define configurations that you want to manage and assess for compliance on devices.

You can specify the *ParentConfigurationItem* parameter to create a child configuration item.
Child configuration items in System Center Configuration Manager are copies of configuration items that retain a relationship to the original configuration item; therefore, they inherit the original configuration from the parent configuration item.
You cannot create child configuration items for mobile devices.

## EXAMPLES

### Example 1: Create a configuration item

```powershell
PS C:\> New-CMConfigurationItem -CreationType MobileDevice -Name "MD_Config88"
```

This command creates a configuration item for mobile devices named MD_Config88.

## PARAMETERS

### -Category

Specifies an array of localized names of the categories to which the configuration item belongs.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: LocalizedCategoryInstanceNames

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreationType

Specifies the type of configuration item.
The acceptable values for this parameter are:

- MacOS
- MobileDevice
- None
- WindowsApplication
- WindowsOS

```yaml
Type: CICreationType
Parameter Sets: New
Aliases: 
Accepted values: None, WindowsApplication, WindowsOS, MacOS, MobileDevice

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specifies a description for a configuration item.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

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

Specifies a name for the configuration item.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentConfigurationItem

Specifies a parent **CMConfigurationItem** object.
To obtain a **CMConfigurationItem** object, use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: NewChild
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

## RELATED LINKS

[Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014)

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](Get-CMConfigurationItemXMLDefinition.md)

[Get-CMConfigurationItemHistory](Get-CMConfigurationItemHistory.md)

[Set-CMConfigurationItem](Set-CMConfigurationItem.md)

[Remove-CMConfigurationItem](Remove-CMConfigurationItem.md)

[Import-CMConfigurationItem](Import-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertTo-CMConfigurationItem](ConvertTo-CMConfigurationItem.md)

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)