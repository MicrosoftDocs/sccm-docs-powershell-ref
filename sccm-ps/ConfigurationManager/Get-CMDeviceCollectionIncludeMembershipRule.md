---
author: aczechowski
description: Gets an Include Collections membership rule for a device collection.
external help file: AdminUI.PS.Collections-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMDeviceCollectionIncludeMembershipRule
titleSuffix: Configuration Manager
---

# Get-CMDeviceCollectionIncludeMembershipRule

## SYNOPSIS
Gets an Include Collections membership rule for a device collection.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByIdAndName
```
Get-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> [-IncludeCollectionName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceCollectionIncludeMembershipRule** cmdlet gets one or more Include Collections membership rules for a device collection.

## EXAMPLES

### Example 1: Get all Include Collections membership rules
```
PS XYZ:\> Get-CMDeviceCollectionIncludeMembershipRule -CollectionName "Device"
```

This command gets all Include Collections membership rules for the collection named Device.

### Example 2: Get Include Collections rules by using the pipeline
```
PS XYZ:\> Get-CMCollection -Name "Device" | Get-CMDeviceCollectionIncludeMembershipRule
```

This command gets the device collection object named Device and uses the pipeline operator to pass the object to **Get-CMDeviceCollectionIncludeMembershipRule**, which gets all Include Collections membership rules for the device collection object.

## PARAMETERS

### -CollectionId
Specifies the ID of a device collection.

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
Specifies the name of a device collection.

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

### -IncludeCollection
Specifies a device collection object included in a membership rule.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

### -IncludeCollectionId
Specifies the ID of a device collection included in a membership rule.

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

### -IncludeCollectionName
Specifies the name of a device collection included in a membership rule.

```yaml
Type: String
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
Aliases:

Required: False
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433)

[Add-CMDeviceCollectionIncludeMembershipRule](Add-CMDeviceCollectionIncludeMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)

[Remove-CMDeviceCollectionIncludeMembershipRule](Remove-CMDeviceCollectionIncludeMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)


