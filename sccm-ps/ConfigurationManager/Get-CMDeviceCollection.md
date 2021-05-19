---
description: Gets one or more device collections in the Configuration Manager hierarchy.
external help file: AdminUI.PS.psm1-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDeviceCollection
---

# Get-CMDeviceCollection

## SYNOPSIS
Gets one or more device collections in the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
Get-CMDeviceCollection [-Name <String>] [<CommonParameters>]
```

### ById
```
Get-CMDeviceCollection -Id <String> [<CommonParameters>]
```

### ByDPGroupName
```
Get-CMDeviceCollection -DistributionPointGroupName <String> [<CommonParameters>]
```

### ByDPGroupId
```
Get-CMDeviceCollection -DistributionPointGroupId <String> [<CommonParameters>]
```

### ByDPGroup
```
Get-CMDeviceCollection -DistributionPointGroup <IResultObject> [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceCollection** cmdlet retrieves collections that contain computers or mobile devices.
For more information about collections, see [Introduction to Collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a device collection by using an ID
```
PS XYZ:\> Get-CMDeviceCollection -CollectionId "9990000D"
```

This command gets the device collection that has the ID 9990000D.

## PARAMETERS

### -DistributionPointGroup
```yaml
Type: IResultObject
Parameter Sets: ByDPGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupId
```yaml
Type: String
Parameter Sets: ByDPGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
```yaml
Type: String
Parameter Sets: ByDPGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
```yaml
Type: String
Parameter Sets: ById
Aliases: CollectionId

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

### System.Object
## NOTES

## RELATED LINKS

[Introduction to Collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections)

[New-CMDeviceCollection](New-CMDeviceCollection.md)


