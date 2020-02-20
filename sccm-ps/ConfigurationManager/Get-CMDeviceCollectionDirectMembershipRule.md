---
author: aczechowski
description: Gets a direct membership rule for a device collection.
external help file: AdminUI.PS.Collections-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMDeviceCollectionDirectMembershipRule
titleSuffix: Configuration Manager
---

# Get-CMDeviceCollectionDirectMembershipRule

## SYNOPSIS
Gets a direct membership rule for a device collection.

## SYNTAX

### ByNameAndName (Default)
```
Get-CMDeviceCollectionDirectMembershipRule -CollectionName <String> [-ResourceName <String>]
 [<CommonParameters>]
```

### ByNameAndValue
```
Get-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject>
 [<CommonParameters>]
```

### ByNameAndId
```
Get-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String> [<CommonParameters>]
```

### ByIdAndValue
```
Get-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject>
 [<CommonParameters>]
```

### ByIdAndId
```
Get-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String> [<CommonParameters>]
```

### ByIdAndName
```
Get-CMDeviceCollectionDirectMembershipRule -CollectionId <String> [-ResourceName <String>] [<CommonParameters>]
```

### ByValueAndValue
```
Get-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject>
 [<CommonParameters>]
```

### ByValueAndId
```
Get-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String>
 [<CommonParameters>]
```

### ByValueAndName
```
Get-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> [-ResourceName <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceCollectionDirectMembershipRule** cmdlet gets one or more direct membership rules for a device collection.

## EXAMPLES

### Example 1: Get a direct membership rule by its name
```
PS XYZ:\> Get-CMDeviceCollectionDirectMembershipRule -CollectionName "Device01"
```

This command gets the direct membership rules for the device collection named Device01.

### Example 2: Get a direct membership rule by using the pipeline
```
PS XYZ:\> Get-CMCollection -Name "Device02" | Get-CMDeviceCollectionDirectMembershipRule
```

This command gets the device collection object named Device02 and uses the pipeline operator to pass the object to Get-CMDeviceCollectionDirectMembershipRule which gets the direct membership rules for the device collection object.

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

### -Resource
Specifies a resource object.
To obtain a resource object, use the **Get-CMResource** cmdlet.

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

### -ResourceId
Specifies the ID of a resource.

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

### -ResourceName
Specifies the name of a resource.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433)

[Add-CMDeviceCollectionDirectMembershipRule](Add-CMDeviceCollectionDirectMembershipRule.md)

[Remove-CMDeviceCollectionDirectMembershipRule](Remove-CMDeviceCollectionDirectMembershipRule.md)

[Get-CMUserCollection](Get-CMUserCollection.md)


