---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
schema: 2.0.0
title: Get-CMUserCollection
---

# Get-CMUserCollection

## SYNOPSIS

Get one or more user collections.

## SYNTAX

### ByName (Default)
```
Get-CMUserCollection [-Name <String>] [<CommonParameters>]
```

### ById
```
Get-CMUserCollection -Id <String> [<CommonParameters>]
```

### ByDPGroupName
```
Get-CMUserCollection -DistributionPointGroupName <String> [<CommonParameters>]
```

### ByDPGroupId
```
Get-CMUserCollection -DistributionPointGroupId <String> [<CommonParameters>]
```

### ByDPGroup
```
Get-CMUserCollection -DistributionPointGroup <IResultObject> [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more user collections.
To get either device or user collections, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.
For more information about collections, see [Introduction to Collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a user collection

This command gets the default user collection **All Users** with ID **SMS00002**.

```powershell
Get-CMUserCollection -CollectionId "SMS00002"
```

## PARAMETERS

### -DistributionPointGroup

Specify a distribution point group object that's associated with this collection. To get this object, use the [Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md) cmdlet.

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

Specify the GUID for a distribution point group that's associated with this collection. This value is the **GroupID** property, which is a standard GUID surrounded by curly brackets, for example, `{537e6303-69eb-4104-bf7b-7baf43ce2352}`.

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

Specify the name of a distribution point group that's associated with this collection.

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

Specify the ID of the user collection to get. This value is the **CollectionID** property, for example, `XYZ00013` or `SMS00002`.

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

Specify the name of the user collection to get.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

For more information on this return object and its properties, see [SMS_Collection server WMI class](/mem/configmgr/develop/reference/core/clients/collections/sms_collection-server-wmi-class).

## RELATED LINKS

[New-CMUserCollection](New-CMUserCollection.md)

[Remove-CMCollection](Remove-CMCollection.md)
[Set-CMCollection](Set-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Introduction to Collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections)
