---
author: aczechowski
description: Gets a software update category.
external help file: AdminUI.PS.Sum.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMSoftwareUpdateCategory
titleSuffix: Configuration Manager
---

# Get-CMSoftwareUpdateCategory

## SYNOPSIS
Gets a software update category.

## SYNTAX

### ByName (Default)
```
Get-CMSoftwareUpdateCategory [-Name <String>] [-TypeName <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMSoftwareUpdateCategory -Id <String> [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByUniqueId
```
Get-CMSoftwareUpdateCategory -UniqueId <String> [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

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

### -Fast
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
```yaml
Type: String
Parameter Sets: ById
Aliases: CategoryInstanceID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: ByName
Aliases: LocalizedCategoryInstanceName, CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeName
```yaml
Type: String
Parameter Sets: ByName
Aliases: CategoryTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UniqueId
```yaml
Type: String
Parameter Sets: ByUniqueId
Aliases: CategoryInstance_UniqueID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_UpdateCategoryInstance
IResultObject#SMS_UpdateCategoryInstance

## NOTES

## RELATED LINKS
