---
author: aczechowski
description: Adds an exclude membership rule to one or more Configuration Manager device collections.
external help file: AdminUI.PS.Collections-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Add-CMDeviceCollectionExcludeMembershipRule
titleSuffix: Configuration Manager
---

# Add-CMDeviceCollectionExcludeMembershipRule

## SYNOPSIS
Adds an exclude membership rule to one or more Configuration Manager device collections.

## SYNTAX

### ByNameAndName (Default)
```
Add-CMDeviceCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollectionName <String>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Add-CMDeviceCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollection <IResultObject>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Add-CMDeviceCollectionExcludeMembershipRule -CollectionName <String> -ExcludeCollectionId <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Add-CMDeviceCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollection <IResultObject>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Add-CMDeviceCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollectionId <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Add-CMDeviceCollectionExcludeMembershipRule -CollectionId <String> -ExcludeCollectionName <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Add-CMDeviceCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollection <IResultObject>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Add-CMDeviceCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollectionId <String>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Add-CMDeviceCollectionExcludeMembershipRule -InputObject <IResultObject> -ExcludeCollectionName <String>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDeviceCollectionExcludeMembershipRule** cmdlet adds a rule that excludes the members of another collection from the device collections where the rule is applied.
You can specify the device collections where the rule is applied by name, ID, or by an object that represents the collections.
You can specify the collection whose members are excluded by name, ID, or an object that represents the collection.

Microsoft System Center Configuration Manager dynamically updates the membership of the device collection on a schedule if the membership of the excluded collection changes.
For more information on these rules, see [Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add an exclude collection rule to a single device collection
```
PS XYZ:\>Add-CMDeviceCollectionExcludeMembershipRule -CollectionId "9990000D" -ExcludeCollectionId "SMSDM001"
```

This command excludes the members of the All Mobile Devices collection, which has the ID SMSDM001, from the device collection, which has the ID 9990000D0.

## PARAMETERS

### -CollectionId
```yaml
Type: String
Parameter Sets: ByIdAndValue, ByIdAndId, ByIdAndName
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
```yaml
Type: String
Parameter Sets: ByNameAndName, ByNameAndValue, ByNameAndId
Aliases: Name

Required: True
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

### -ExcludeCollection
```yaml
Type: IResultObject
Parameter Sets: ByNameAndValue, ByIdAndValue, ByValueAndValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeCollectionId
```yaml
Type: String
Parameter Sets: ByNameAndId, ByIdAndId, ByValueAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeCollectionName
```yaml
Type: String
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValueAndValue, ByValueAndId, ByValueAndName
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Introduction to Collections in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682177(v=technet.10))

[Get-CMDeviceCollectionExcludeMembershipRule](Get-CMDeviceCollectionExcludeMembershipRule.md)

[Remove-CMDeviceCollectionExcludeMembershipRule](Remove-CMDeviceCollectionExcludeMembershipRule.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
