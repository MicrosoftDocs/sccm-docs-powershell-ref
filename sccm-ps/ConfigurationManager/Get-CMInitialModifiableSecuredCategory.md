---
description: Gets modifiable secured categories.
external help file: AdminUI.PS.Migration.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMInitialModifiableSecuredCategory
---

# Get-CMInitialModifiableSecuredCategory

## SYNOPSIS
Gets modifiable secured categories.

## SYNTAX

### SearchById (Default)
```
Get-CMInitialModifiableSecuredCategory [-Id <String>] [-ObjectTypeId <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByName
```
Get-CMInitialModifiableSecuredCategory [-ObjectTypeId <String>] [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMInitialModifiableSecuredCategory** cmdlet gets modifiable secured categories from Configuration Manager.

Note: This cmdlet was previously known as **Get-CMInitModifiableSecuredCategory** in System Center 2012 Configuration Manager SP1.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get information about all your modifiable secured categories
```
PS XYZ:\> Get-CMInitialModifiableSecuredCategory
```

This command returns information about all your modifiable secured categories.

### Example 2: Get information about a specific modifiable secured category
```
PS XYZ:\> Get-CMInitialModifiableSecuredCategory -ID "121989"
```

This command returns information about the modifiable secured category that has the ID 121989.

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
Specifies an identifier in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: CategoryId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectTypeId
Specifies an ID for an object type.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Configuration Manager cmdlets](ConfigurationManager.md)
