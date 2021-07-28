---
description: Gets modifiable secured categories.
external help file: AdminUI.PS.dll-Help.xml
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
Get-CMInitialModifiableSecuredCategory [-Name <String>] [-ObjectTypeId <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMInitialModifiableSecuredCategory** cmdlet gets modifiable secured categories from Configuration Manager.

Note: This cmdlet was previously known as **Get-CMInitModifiableSecuredCategory** in System Center 2012 Configuration Manager SP1.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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
Accept wildcard characters: True
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_InitModifiableSecuredCategory
### IResultObject#SMS_InitModifiableSecuredCategory
## NOTES

## RELATED LINKS
